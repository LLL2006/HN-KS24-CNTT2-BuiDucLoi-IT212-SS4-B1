Đáp án lựa chọn: B

Phương án B là lựa chọn tối ưu nhất vì nó chứa đầy đủ các thành phần quan trọng của một prompt chất lượng, giúp AI tạo ra kết quả chính xác, ổn định và giảm nguy cơ thay đổi logic nghiệp vụ.

Phân tích theo 5 thành phần Prompt
1. Vai trò (Role)

Phương án B:

"Hãy đóng vai trò là một Java Senior Developer"

Điểm mạnh:

Xác định rõ AI phải hành xử như một lập trình viên Java có kinh nghiệm.
Giúp AI ưu tiên các nguyên tắc như Clean Code, refactor an toàn, khả năng bảo trì, thay vì chỉ viết ngắn hơn.
Tăng khả năng AI áp dụng đúng kỹ thuật guard clauses (return sớm).

Đánh giá:
✅ Có vai trò rõ ràng.

Phương án A và C:

Không có chỉ định vai trò.
AI có thể đưa ra nhiều cách xử lý khác nhau không theo tiêu chuẩn kỹ thuật mong muốn.
2. Mục tiêu (Goal)

Phương án B:

"tái cấu trúc logic rẽ nhánh lồng nhau phức tạp của class DiscountService thành các câu lệnh điều kiện bảo vệ (guard clauses / return sớm)"

Điểm mạnh:

Mục tiêu rất cụ thể.
Chỉ rõ kỹ thuật cần áp dụng (guard clauses).
Giảm khả năng AI chọn hướng khác như dùng Stream, switch, Strategy Pattern hoặc lambda.

Đánh giá:

✅ Mục tiêu rõ ràng và đúng yêu cầu đề bài.

Phương án A:

"để nó đẹp hơn"

Vấn đề:

“đẹp hơn” rất mơ hồ.
AI không biết:
đẹp về giao diện?
tối ưu hiệu năng?
chuẩn Clean Code?
giảm số dòng?

Phương án C:

"viết ngắn gọn nhất có thể"

Vấn đề:

Tập trung vào độ ngắn thay vì chất lượng thiết kế.
Dễ dẫn đến việc AI hy sinh tính dễ đọc.
3. Ngữ cảnh (Context)

Phương án B:

"logic rẽ nhánh lồng nhau phức tạp của class DiscountService"

Điểm mạnh:

Nêu đúng vấn đề thực tế:
nested if-else khó bảo trì.
AI hiểu mục tiêu là xử lý vấn đề thiết kế chứ không phải viết lại từ đầu.

Đánh giá:

✅ Có ngữ cảnh rõ ràng.

Phương án A:

Không có ngữ cảnh.

Phương án C:

Ngữ cảnh thiếu và hướng sai trọng tâm.
4. Ràng buộc (Constraints)

Phương án B:

Giữ nguyên logic nghiệp vụ tính chiết khấu ban đầu
Không thay đổi kiểu dữ liệu đầu vào/đầu ra
Sử dụng Java 11

Đây là phần quan trọng nhất.

Điểm mạnh:

Giữ nguyên nghiệp vụ

Tránh lỗi logic khi refactor.
Refactor chỉ thay đổi cấu trúc, không thay đổi hành vi.

Giữ nguyên input/output

Tránh AI đổi sang enum, Optional, BigDecimal hoặc kiểu khác.

Java 11

Kiểm soát môi trường thực thi.

Đánh giá:

✅ Ràng buộc đầy đủ.

Phương án A:

Không có ràng buộc.

Phương án C:

Ép dùng Stream API dù Stream không phù hợp với xử lý điều kiện phân nhánh.
5. Định dạng đầu ra (Format)

Phương án B:

"Trình bày kết quả dưới dạng khối mã nguồn Java hoàn chỉnh kèm giải thích ngắn bằng tiếng Việt"

Điểm mạnh:

Quy định rõ cấu trúc kết quả.
Dễ đọc và dễ sử dụng.
Tránh AI trả lời lan man.

Đánh giá:

✅ Có định dạng rõ ràng.

Phương án A và C:

Không quy định định dạng.
Tổng kết đánh giá 5 thành phần
Thành phần	A	B	C
Vai trò	❌	✅	❌
Mục tiêu	❌	✅	⚠️
Ngữ cảnh	❌	✅	⚠️
Ràng buộc	❌	✅	❌
Định dạng	❌	✅	❌

Phương án B đạt 5/5 thành phần, là prompt hoàn chỉnh nhất.

Phân tích lý do loại trừ phương án A

Phương án A:

"Tái cấu trúc code Java trên để nó đẹp hơn."

Nhược điểm

1. Mục tiêu mơ hồ

“đẹp hơn” là khái niệm chủ quan.
AI có thể:
đổi tên biến
format lại code
thêm comment
chuyển sang switch-case
dùng Strategy Pattern

Nhưng chưa chắc sử dụng guard clauses.

2. Không có ràng buộc bảo toàn nghiệp vụ

Nguy cơ:

AI có thể sửa thành:

if (type.equals("VIP") && amount > 1000)
    return amount * 0.25;

và vô tình làm mất trường hợp:

VIP + amount <=1000

=> Sai logic nghiệp vụ.

3. Không có yêu cầu về Java version

AI có thể dùng:

switch expression
record
cú pháp Java mới

gây lỗi nếu dự án dùng Java 11.

Phân tích lý do loại trừ phương án C

Phương án C:

"bỏ bớt if-else lồng nhau đi và sử dụng cấu trúc Java Stream API để viết ngắn gọn nhất có thể."

Nhược điểm

1. Stream API không phù hợp

Stream phù hợp cho:

xử lý collection
map
filter
reduce

Trong bài toán này chỉ là:

điều kiện nghiệp vụ
phân nhánh logic

Ép dùng Stream sẽ tạo code phức tạp bất thường.

Ví dụ AI có thể sinh:

return Stream.of(...)
       .filter(...)
       .findFirst()
       .orElse(0.0);

Code này:

khó đọc hơn
khó debug
trái với tinh thần Clean Code

2. "Viết ngắn gọn nhất có thể" dễ gây tác dụng ngược

AI có thể tạo:

return type.equals("VIP")
? (amount>1000?(isHoliday?amount*0.25:amount*0.20):amount*0.15)
: (amount>500?(isHoliday?amount*0.10:amount*0.05):0);

Mặc dù ít dòng hơn nhưng:

rất khó đọc
khó bảo trì
không đúng mục tiêu refactor

3. Không có ràng buộc bảo toàn nghiệp vụ

Nguy cơ:

AI tối ưu quá mức.
Thay đổi logic tính chiết khấu.
Kết luận

Phương án B là lựa chọn tối ưu nhất vì:

Xác định rõ vai trò
Có mục tiêu cụ thể
Cung cấp ngữ cảnh
Đưa ra ràng buộc quan trọng
Quy định định dạng đầu ra   