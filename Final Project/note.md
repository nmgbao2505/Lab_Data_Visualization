Xét nhóm khách sạn `City Hotel` (với 8 mã phòng khác nhau):

- Với các mã phòng `A`, `B`, `C` và `K`: Trong số các hành khách đến lưu trú tại khách sạn thuộc nhóm `City Hotel` và được sắp xếp vào ở một trong các phòng `A`, `B`, `C` hoặc `K`, ta thấy có khoảng 80% hành khách sẽ tạo ra giá trị doanh thu rơi vào khoảng (-7.001, 123.0]. Có khoảng 20% hành khách tạo ra doanh thu trong khoảng (123.0, 253.0]. Và có rất ít hành khách (hoặc thậm chí không có hành khách nào) trong nhóm này tạo ra giá trị `adr` lớn hơn 253 cho các khách sạn `City Hotel`.

- Với các mã phòng `D`, `E` và `F`: Trong số các hành khách đến lưu trú tại khách sạn thuộc nhóm `City Hotel` và được sắp xếp vào ở một trong các phòng `D`, `E` hoặc `F`, ta thấy có hơn một nửa số hành khách tạo ra giá trị doanh thu rơi vào khoảng (123.0, 253.0]. Các hành khách còn lại chủ yếu sẽ đem lại ít doanh thu hơn cho khách sạn, giá trị `adr` thuộc đoạn (-7.001, 123.0]. Tuy có một số ít hành khách tạo ra giá trị `adr` lớn hơn 253 nhưng số lượng mẫu dữ liệu này là quá ít nên ta sẽ không đề cập chi tiết.

- Đặc biệt nhất là mã phòng `G`: Trong số các hành khách lưu trú tại khách sạn thuộc loại `City Hotel` và được sắp xếp ở phòng có mã `G`, ta thấy có hơn 56% hành khách tạo ra giá trị `adr` dao động trong khoảng (123.0, 253.0]. Nổi bật nhất là có hơn 20% hành khách tạo ra giá trị `adr` rơi vào khoảng (253.0, 383.0]. Phần lớn các hành khách còn lại sẽ đem lại doanh thu trung bình rơi vào khoảng (-7.001, 123.0]. Như vậy, mã phòng `G` là loại phòng có nhiều tiềm năng đem lại nhiều thu nhập cho khách sạn.

- Như vậy, với các khách sạn trong nhóm `City Hotel`, các chủ khách sạn có thể tăng thêm số lượng phòng có mã `F` và `G` để có thể tối đa hóa doanh thu cho khách sạn.

Xét nhóm khách sạn `Resort Hotel` (với 10 mã phòng khác nhau):

- Với các mã phòng `A`, `B`, `D`, `E`, `I` và `L`: Trong số các hành khách đến lưu trú tại khách sạn thuộc nhóm `Resort Hotel` và được sắp xếp vào ở một trong các phòng `A`, `B`, `D`, `E`, `I` hoặc `L`, ta thấy phần lớn hành khách sẽ tạo ra giá trị doanh thu trung bình ở bin thứ nhất, giá trị `adr` rơi vào khoảng (-7.001, 123.0]. Chỉ có một lượng nhỏ hành khách có thể tạo ra giá trị `adr` rơi vào khoảng (123.0, 253.0] và có rất ít hành khách có thể tạo ra giá trị `adr` lớn hơn 253.

- Với các mã phòng `C` và `F`: Trong số các hành khách đến lưu trú tại khách sạn thuộc nhóm `Resort Hotel` và được sắp xếp vào ở một trong các phòng `C` hoặc `F`, ta thấy có khoảng 60% hành khách tạo ra giá trị `adr` trong khoảng (-7.001, 123.0]. Có khoảng hơn 30% hành khách tạo ra giá trị `adr` trong khoảng (123.0, 253.0]. Đồng thời, cũng có khoảng 5% hành khách tạo ra doanh thu nhiều hơn cho khách sạn, giá trị `adr` lớn hơn 253.

- Đặc biệt nhất là mã phòng `G` và `H`: Phần lớn hành khách lưu trú tại các khách sạn thuộc nhóm `Resort Hotel` và ở một trong các mã phòng `G` hoặc `H` thường đem lại rất nhiều lợi nhuận cho khách sạn. Có khoảng 50% hành khách tạo ra lợi nhuận ở mức (bin) 2, giá trị `adr` thuộc đoạn (123.0, 253.0]. Đồng thời có khoảng 15% hành khách tạo ra lợi nhuận ở mức (bin) 3 và 4, giá trị `adr` lớn hơn 253.

- Như vậy, với các khách sạn trong nhóm `Resort Hotel`, các chủ khách sạn có thể tăng thêm số lượng phòng có mã `H`, `G`, `C` và `F` để có thể tối đa hóa doanh thu cho khách sạn.

