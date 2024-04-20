Có vẻ như thuộc tính "SepalLengthCm" chưa phải là một công cụ đủ mạnh để giúp ta dễ dàng phân biệt giữa các loài hoa diên vĩ khác nhau.

phân bố khác nhau của thuộc tính chiều rộng lá đài ở các loài hoa khác nhau. Đây có thể là dấu hiệu đáng mừng cho thấy "SepalWidthCm" sẽ là một thuộc tính quan trọng giúp ta dễ dàng phân biệt giữa các loài hoa diên vĩ khác nhau. Và ta có thể tập trung phân tích sâu hơn vào thuộc tính "SepalWidthCm" để làm rõ điều này.

---
Quá trình phân tích phân bố chiều dài cánh hoa ở các loài hoa Iris khác nhau có thể giúp ta hiểu rõ hơn về sự đa dạng của các loài hoa Iris và cách chúng có thể được phân loại dựa trên đặc điểm này.

tránh phải sử dụng các đặc trưng không có nhiều ý nghĩa trong viec76

trong việc phân loại các loài hoa Iris khác nhau.

phân tích trên

---


Biểu đồ thể hiện 
Bảng mô tả các đại lượng thống kê cho

phân bố cho thuộc tính "SepalLengthCm" của loài hoa "Iris-setosa".

cho
mô tả

import numpy as np
import scipy.stats

def mean_confidence_interval(data, confidence=0.95):
    a = 1.0 * np.array(data)
    n = len(a)
    m, se = np.mean(a), scipy.stats.sem(a)
    h = se * scipy.stats.t.ppf((1 + confidence) / 2., n-1)
    return m, m-h, m+h
mean_confidence_interval(setosa_df[feature])
---



thì

và loại bỏ các

Trong trường hợp ta khám phá ra các thông tin quan trọng về đặc điểm của loài hoa Iris, thì kết quả này có thể được phát triển 

đặc điểm nổi bật trong phân bo61 

hoặc 

Đồng thời, việc tập trung phân tích, xử lý trên các đặc điểm nổi bật sẽ giúp tiết kiệm "chi phí" (như: thời gian, tiền bạc, v.v.) trong việc thu thập và xử lý dữ liệu.


cung cấp thông tin quan trọng cho các nghiên cứu liên quan đến việc phân loại cây cối dựa trên đặc điểm hình thái.

### 4.5. Chia bộ dữ liệu thành tập chứa các cột có kiểu dữ liệu dạng số (biến định lượng) và tập chứa các cột có kiểu dữ liệu dạng phân loại (biến định tính)

phân bố

Thông qua việc phân tích phân bố chiều dài cánh hoa ở các loài hoa Iris khác nhau

mang tính chất quyết định trong việc phân loại các loài hoa Iris khác nhau

là yếu tố

Việc trả lời câu hỏi này sẽ mang lại cho ta một số lợi ích:

- Bằng cách xem xét cả chiều dài và chiều rộng của cánh hoa, ta sẽ có cái nhìn toàn diện hơn về đặc điểm hình thái của các loài hoa Iris và cách chúng có thể được phân loại dựa trên kích thước cánh hoa.
- Nếu kích thước cánh hoa là yếu tố đủ để phân loại chính xác các loài hoa Iris, ta có thể tối ưu hóa quá trình phân loại bằng cách chỉ tập trung vào các đặc điểm này, giảm bớt sự phức tạp trong việc thu thập và xử lý dữ liệu so với việc xem xét một số đặc điểm khác nhau.
- Trả lời được câu hỏi này có thể giúp ta tiết kiệm thời gian và công sức trong quá trình nghiên cứu hoặc phát triển mô hình phân loại hoa Iris, bằng cách tập trung vào một số đặc điểm quan trọng nhất.
- Nếu kích thước cánh hoa là yếu tố quyết định, thông tin này có thể được áp dụng trong các ứng dụng thực tiễn như trong nông nghiệp, sinh học, hoặc các lĩnh vực khác đòi hỏi phân loại hoa Iris.
- Kết quả từ việc trả lời câu hỏi này có thể làm nền tảng cho các nghiên cứu tiếp theo về hoa Iris, hoặc cung cấp thông tin quan trọng cho các nghiên cứu liên quan đến phân loại dựa trên đặc điểm hình thái của cây cối.

Liệu kích thước (chiều dài và chiều rộng) cánh hoa có phải là yếu tố đủ để phân loại chính xác các loài hoa Iris (diên vĩ) khác nhau hay không?

Chúng ta sẽ thực hiện quy trình phân tích khám phá dữ liệu (EDA) lên bộ dữ liệu Iris để khám phá ra các thuộc tính hữu ích có thể giúp ta giải quyết bài toán phân lớp các loài hoa khác nhau. Việc tìm được các thuộc tính như vậy sẽ giúp ta dễ dàng dự đoán giá trị nhãn của bất kỳ mẫu dữ liệu mới nào trong tương lai.

Mục tiêu "khám phá ra các thuộc tính hữu ích có thể giúp ta giải quyết bài toán phân lớp các loài hoa Iris khác nhau" có thể được cụ thể hóa ra thành các câu hỏi sau:

và xử lý các cột có giá trị bất thường

mô tả

Thuộc tính

Ta sử dụng

Chia bộ dữ liệu thành hai tập con: tập chứa các cột có kiểu dữ liệu dạng số (biến định lượng) và tập chứa các cột có kiểu dữ liệu dạng phân loại (biến định tính)

tập biến định lượng và tập biến định tính

và thực hiện tiền xử lý (nếu cần)

color_map = {
"Iris-setosa": "skyblue",
"Iris-versicolor": "lightcoral",
"Iris-virginica": "lightgreen"
}

---

Thay vì sử dụng thuộc tính "dtypes" của đối tượng DataFrame, ta có thể phân tích dữ liệu trong mỗi cột để xác định kiểu dữ liệu của cột tương ứng.

Nhận xét:

Để dễ dàng so sánh phân bố chiều dài lá đài của ba loài hoa, ta sẽ trực quan hóa dữ liệu trên cùng một biểu đồ mật độ và dùng màu sắc để chú thích cho phân bố của mỗi loài hoa.

---

- Sau khi phân tích các đặc trưng về kích thước của cánh hoa và lá đài trong bộ dữ liệu hoa Iris, ta thấy rằng chiều dài và chiều rộng cánh hoa là các đặc trưng hữu ích giúp phân loại các loài hoa Iris một cách khá chính xác. Trong khi đó, kích thước lá đài không thực sự là một đặc trưng đủ tốt để giải quyết bài toán phân lớp các loài hoa Iris do mức độ chồng chéo dữ liệu ở các thuộc tính này diễn ra khá phức tạp.

- Bằng cách kết hợp chiều dài và chiều rộng cánh hoa, ta có thể phân loại chính xác hầu hết mẫu dữ liệu thuộc loài "Iris-setosa". Riêng với hai loài "Iris-versicolor" và "Iris-virginica", do phân bố kích thước cánh hoa ở hai loài này không tách biệt hoàn toàn với nhau nên ta không thể phân biệt chính xác hai loài này bằng một mô hình đơn giản. Mặc dù ta có thể xây dựng một mô hình phức tạp để đạt độ chính xác tuyệt đối trên bộ dữ liệu đang phân tích nhưng mô hình đó sẽ có không có tính tổng quát hóa và không phải là mục tiêu mà ta muốn đạt được.

- Như vậy, để tiếp tục cải thiện hiệu suất của mô hình, ta có thể thu thập thêm dữ liệu mới cũng như các đặc trưng khác ở hoa Iris. Sau đó, ta thực hiện quy trình phân tích dữ liệu để chọn ra các đặc trưng nổi bật giúp phân biệt các loài hoa khác nhau. Khi này, thay vì xây dựng mô hình phức tạp chỉ đơn thuần "học thuộc lòng" dữ liệu huấn luyện, ta có thể sử dụng mô hình đơn giản hơn với khả năng giải thích và tổng quát hóa cao, đảm bảo hiệu suất hoạt động tốt trên cả dữ liệu huấn luyện và dữ liệu mới trong tương lai.
