# How to build a complete website with python
0. Các bước xây dựng website
```code 
- Thiết kế nội dung (trang web làm gì, có những chức năng gì)
- Thiết kế cơ sở dữ liệu 
- Vẽ mockup (vẽ các page trên giấy) 
- Lựa chọn ngôn ngữ lập trình và các thư viện 
- Python + Flask + Material + Bootstrap + MySQL + Angular 2
- Tạo cơ sở dữ liệu  
- Tạo trang quản lí người dùng (Backend)
	+ Phân chia page cho mỗi người
- Tạo trang homepage (Frondend)
	+ Phân chia page cho mỗi người

- Chạy thử trang web 
- Mua hosting, mua tên miền 
- Cài Đặt Mã Nguồn Website Lên Hosting
- Chuyển đổi tên miền. 
```

0. Đọc hiểu khái niệm Frondend, Backend và Fullstack 
```code 
	- Frondend là giao diện người dùng, ví dụ khi truy cập vào trang web amazon.com thì các trang nhu homepage của nó gọi là frondend, người dùng trực tiếp sử dụng và tương tác trên đó. 
	- Hoặc khi ta tạo tài khoản trên trang amazon.com và đăng nhập vào tài khoản, ta có thể xem được các trang như giỏ hàng, số thông tin tài khoản.... Đây cũng là những trang frondend 

	- Backend là giao diện của nhà quản trị, người quản lí website đó. Họ sẽ có những trang để quản lí tài khoản của người dùng. (Họ có thể xóa người dùng ra khỏi hệ thống, thêm người dùng mới vào hệ thống). Người dùng bình thường sẽ không nhìn thấy được những trang như vậy.

	https://techmaster.vn/posts/33487/lap-trinh-web-front-end-vs-back-end-vs-full-stack
```

1. Học kiến thức về Frondend trước 
```code 
1. HTML và CSS 
	- HTML là khung xương của trang web, còn CSS thì là trang trí cho trang web. HTML có thể ví như con người không mặc gì, khi mặc trang phục vào thì đó là CSS. 
	(CSS:  Định dạng thiết kế, bố cục, phong cách, canh lề của trang web.)
	
	https://www.w3schools.com/html/
	https://www.w3schools.com/css/default.asp

2. Javascript 
	- Nếu chỉ xây dựng website với HTML với CSS thì website đó là website tĩnh, tức là không có tương tác với người dùng cả. Vì chưa có kết nối với cơ sở dữ liệu. 
	- Javascript là ngôn ngữ lập trình mang đến sự sinh động cho website. Đồng thời nó cũng có thể giúp tối code HTML khi trang có những thành phần giống nhau.
	- Nên đọc [bài viết này](https://www.hostinger.vn/huong-dan/javascript-la-gi/) để hiểu thêm
	
	- Như ta biết, các ngôn ngữ lập trình cần trình biên dịch để chạy. Còn javascript thì không cần trình biên dịch vẫn có thể chạy trực tiếp trên website.
	- Đây là điểm mạnh cũng như nhược điểm vì chúng nó có thể xem được mã nguồn của javascript ngay trên trình duyệt.
	
	https://www.w3schools.com/js/default.asp

===> Đến đây là ta có thể xây dựng được các trang web frondend 1 cách rất dễ dàng. Tuy nhiên, trang web chỉ là trang web tĩnh, chưa có cơ sở dữ liệu (chưa có ngôn ngữ lập trình backend để kết nối đến server) và đồng thời việc code CSS và Javascript sẽ rất mệt nếu trang web tĩnh lớn.

3. Bootstrap và JQuery 
	- Bootstrap là thư viện của CSS, có thể hiểu là CSS là ngôn ngữ trang trí rất căn bản, để trang trí 1 thành phần thì phải viết cả đống code. Còn Bootstrap nó đã xây dựng sẵn những trang phục rất đẹp cho website dựa trên CSS. Giờ chỉ việc gọi chúng ra và dùng, không cần code lại bằng CSS. Như vậy vừa nhanh là đỡ tốn thời gian.
	
	- JQuery tương tự là thư viện của Javascript, nó cũng xây dựng trên javascript, có rất nhiều thành phần hay có thể dùng sẵn mà không phải code lại bằng javascript.
	
	https://www.w3schools.com/bootstrap4/default.asp
	https://www.w3schools.com/jquery/default.asp
	
4. AngularJS - Angular version 1(Giờ không dùng nữa)
	- AngularJS là thư viện rất lớn có thể làm thay được tất cả HTML, CSS và Javascript. 
	- Thay vì phải code cả 3 loại trên, AngularJS nó có sẵn các thành phần và chỉ việc gọi ra dùng.
	- Tuy nhiên hiện nay người ta không dùng nữa vì nó đã có thư viện khác khủng hơn. 
	
	https://www.w3schools.com/angular/default.asp

5. Angular 2 - Angular version 2 (và các version về sau)
	- Angular 2 là sự khác biệt hoàn toàn với AngularJS (Angular 1). Hiện nay người ta đều dùng phiên bản này.
	- https://angular.io/docs
	- Tạo 1 website frondend hoặc backend quá dễ dàng với vài câu lệnh.
	
==> Còn rất nhiều thư viện hoặc ngôn ngữ lập trình khác mà không đề cập ở đây như: SASS, Ajax, Material, Materialize CSS, React, ....
```

2. Học kiến thức về Backend 
```code 
- Để khiến cho máy chủ, ứng dụng, và cơ sở dữ liệu có thể giao tiếp được với nhau, các lập trình viên back-end sử dụng các ngôn ngữ server-side như PHP, Ruby, Python, Java, và .Net để xây dựng một ứng dụng, và các công cụ như MySQL, Oracle, và SQL Server để tìm kiếm, lưu trữ, hoặc thay đổi dữ liệu và phục vụ trở lại tới người dùng trong phần front-end. Các công việc tuyển dụng lập trình viên back-end cũng thường yêu cầu kinh nghiệm về các framework PHP như Zend, Symfony, và CakePHP; có kinh nghiệm với các phần mềm quản lý phiên bản như SVN, CVS, hoặc Git; và kinh nghiệm với Linux trong việc phát triển và triển khai hệ thống.

- Đến đây thì có 2 cách học: 
	+ 1 là nhảy thẳng vào học ( Python + Flask ) + MySQL để tạo backend 
	+ 2 là học PHP + MySQL để tạo backend, sau đó mới chuyển qua ( Python + Flask ) + MySQL.
- Tại sao lại có cách thứ 2, vì đơn giản PHP là ngôn ngữ lập trình backend dễ học nhất, nó giúp ta hình dung được cách phía server và client giao tiếp với nhau ra sao. Khi đã nắm được các khái niệm căn bản thì việc chuyển qua dùng Python hay Java rất đơn giản.

1. PHP 
	https://www.w3schools.com/php/default.asp

2. MySQL 
	https://www.w3schools.com/sql/default.asp
	
3. Python + Flask 
	https://www.fullstackpython.com/flask.html

```

3. Xây dựng website hoàn chỉnh 
```code
- Cách làm nhanh nhất là: CSS + HTML + Javascript + PhP + MySQL 
	https://www.udemy.com/course/build-a-news-website-using-php-and-mysql/

- Cách làm liên quan đến Python:  HTML + CSS + JavaScript + Flask Python + MySQL 
	https://www.youtube.com/watch?v=MwZwr5Tvyxo
	https://www.youtube.com/watch?v=zdgYw-3tzfI

- Cách làm nhanh sử dụng framework: Angular 2 + Flask Python + MySQL 
	https://www.youtube.com/watch?v=6bL7n9aP6e0
	https://www.youtube.com/watch?v=LOrJ3a70Bw8
```



