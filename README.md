# Câu 1 : Tại sao không nên dùng bản alpha cho dự án của mình?
## *Trả lời* : 
Lý do không nên sử dụng bản alpha vì bản là bản thử nghiệm và không có tính ổn định
# Câu 2 : Underlying stylesheet preproccessor(USP) thay đổi từ BS3->4 như thế nào? Optional: nêu vài điểm khác biệt giữa 2 loại USP?
## *Trả lời* :
Từ Bootstrap 3 -> Bootstrap4 thay đổi sử dụng SASS thay cho LESS 
Vài điểm khác biệt giữa LESS và SASS :
- Sass dễ sử dụng, cung cấp nhiều khả năng tùy biến hơn
- Sass thân thiện với lập trình viên 
- SASS trong Ruby, LESS trong Javascript
- Khai báo biến : LESS khai báo biến bằng @ còn SASS khai báo biến bằng $
- Về kế thừa : LESS không có kế thừa (từ version 1.4.0 mới có, cấu trúc &:extend(tên_class) ). SASS kế thừa bằng cấu trúc @extend ten_class
- Các mệnh đề điều kiện : LESS không hỗ trợ . SASS có thể sử dụng các mệnh đề if, else , các vòng lặp for, while …
- Phạm vi biến : LESS chia ra hai loại : biến toàn cục và biến cục bộ . SASS giá trị biến sẽ tự động thay đổi từ vị trí đó trở xuống
- Quy tắc xếp chồng : Cả LESS và SASS đều có quy tắc xếp chồng. Tuy nhiên SASS có thêm chức năng xếp chồng cho các thuộc tính cá nhân 
- Định đầu ra : LESS không thiết lập đầu ra .SASS cung cấp 4 phương thức đầu ra : Quy tắc xếp chồng (nested),  compact (ví dụ @mixin), compressed(nén lại, bạn sẽ thấy khi biên dịch file .scss -> .css) and expanded (bao gồm mọi tùy chọn có sẵn với bản cập nhật để hỗ trợ trong tương lai).
- Tính toán : 
  - SASS sẽ thông báo đầy đủ nếu phép toán sử dụng sai 
  - LESS thông báo lỗi không đầy đủ 
- LESS có nhiều nguồn tài liệu học thân thiện hơn SASS
- Hiện SASS đang được phát triển trong Ruby. còn LESS chuyển sang nodejs như vậy về khả năng linh hoạt thì LESS có xu thế tốt hơn
# Câu 3 : Ngoài USP mới ra thì BS4 có những gì mới? (nói càng cụ thể càng tốt).
## *Trả lời* :
- Nhỏ hơn , nhẹ hơn chỉ với 88kb
- Hệ grid mới : Extra Small(xs<34rem), Small(sm>34rem),Medium(md>48rem), Large(lg>62rem),Extra-Large(xl>75rem)
- Bỏ support IE8
- Boostrap card sẽ thay thế wells,thumbnails và panels trong bootstrap 3.
- Support flexbox
-  Các class tiện ích mới .clear-fix spacing class (margin, padding).
# Câu 4 : Điểm mạnh của flexbox : 
## *Trả lời* : 
-các thành phần nằm trong container sẽ được sắp xếp, căn chỉnh gọn gàng đẹp đẽ ngay cả khi kích thước của thành phần chưa được xác định trước
-Với việc hỗ trợ đa dạng mục đích sử dụng người dùng, Flexbox cho phép các nhà phát triển web, sắp xếp các phần tử trên web một cách linh hoạt theo ý đồ của chính họ, chỉ với vài dòng lệnh đơn giản, các phần tử của website đã được sắp xếp theo đúng ý đồ của chúng ta và cũng đảm bảo việc Responsive cho các phần tử đó trên web, giảm tải việc code cho các nhà phát triển
-Flexbox chỉ hỗ trợ IE từ phiên bản 11 trở lên nên nếu phát triển website chạy trên Browser mới nhất của IE thì dùng Flexbox là sự lựa chọn tốt nhất.
# Câu 5:Nêu 1 số khác nhau giữa ES6 với ES5? BS4 sử dụng gì để compile Javascript
## *Trả lời* : 
- Từ khóa `let`
- Từ khóa `const`
-  Arrow function : ECMAScript 6 làm đơn giản hóa cách chúng ta viết các anonymous functions (hàm nặc danh), khi chúng ta có thể hoàn toàn bỏ qua từ khóa “function”. Chúng ta chỉ cần sử dụng cú pháp mới cho các arrow function, đặt tên sau ký hiệu mũi tên `=>`. Bên cạnh đó còn có sự khác nhau quan trọng giữa regular function (hàm chính quy) và arrow function, đó là arrow function không nhận giá trị `this` một cách tự động như các hàm được xác định bằng từ khóa `function`. Về phương diện từ vựng, Arrow functions kết giá trị `this` vào phạm vi hiện tại. Điều này có nghĩa là chúng ta có thể dễ dàng tái sử dụng từ khóa `this` trong inner function.
- Toán tử `spread` mới :Toán tử spread mới được đánh dấu bằng 3 dấu chấm (…), và chúng ta có thể sử dụng nó để đánh dấu nơi có nhiều mục được chờ đợi. Một trong những trường hợp sử dụng phổ biến nhất của toán tử spread là chèn các element của một array (mảng) vào một array khác
- Các giá trị mặc định dành cho tham số & các rest parameter mới : Đối với ECMASScript 6, chúng ta có thêm các giá trị vào các parameter (tham số) của một hàm
- Câu lệnh for…of mới.
- Template Literals
- Các class (lớp) : Trong các lớp của ES6 được khai báo với từ khóa mới class, và cần phải có method constructor() - được gọi khi một đối tượng mới được tạo ra bằng cách sử dụng cú pháp new myClass(). Ngoài ra còn có thể mở rộng các lớp mới cùng với cú pháp class Child extends Parent mà chúng ta đã quen thuộc từ các ngon ngữ khác như PHP. Bạn cũng nên lưu ý rằng: không giống như khai báo biến và hàm, sự khai báo class thì KHÔNG có trong ECMAScript 6
- Keyword yield và cú pháp function*().
-Trả về nhiều giá trị đồng thời trong 1 hàm
-.Các tham số mặc định trong hàm : tự động điền giá trị tham số đầu vào theo thứ tự truyền vào tương ứng
- Sử dụng "..." vai trò như định nghĩa một mảng động
**BS 4 sử dụng npm vs webpack để compile Javascript**
# Câu 6: Cách ghi đè variable của bootstrap?
- Tạo `_variables.scss` và ghi đè lại thuộc tính css
# Câu 7 : Mô tả  basic workflow của sass với bs4 được giới thiệu trong video?
- B1: Tạo file `app.scss`và `_variables.css` có nội dung giống file `app.scss`và `_variables.css` của bootstrap rồi comment lại tất cả nội dung ,còn `_base.scss` viết css cần thêm.
- B2 : Sử dụng Ruby để complie sass sang css . Khi sử dụng đến phần nào của Bootstrap thì ta bỏ comment phần đó trong file `app.scss`. mới được tạo
- B3 : Dùng ruby để build ra file app.css.. t sử dụng file app.css trong project của mình
