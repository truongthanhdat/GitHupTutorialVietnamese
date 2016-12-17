# Hướng dẫn sử dụng github cơ bản

## Trước tiên ta nói về Git là gì:

+ Git là một phần mềm quản lý mã nguồn phân tán được phát triển bởi Linus Torvalds  vào năm 2005. Git hiện giờ là một trong những phần mềm quản lý mã nguồn phổ biến nhất. Git gần như được hỗ trợ trên tất cả các nền tảng hệ điều hành (Windows, Mac OSX, Linux, ...). Việc cài đặt git khá dễ dàng, đối với người dùng Windows, Mac OSX có thể lên trang chủ https://git-scm.com để tải và cài đặt, người dùng Linux có thể tải thông qua lệnh apt-get install git.

## Git có thể hai cách sử dụng:

+ Dùng phần mềm của bên thứ 3: Một phần mềm có tên Source Tree cho phép người dùng có thể giao tiếp với git thông qua giao GUI. Tuy nhiên đây là phần mềm được phát triển trên nền tảng JAVA, các thao tác thực hiện khá chậm và việc thực hiện tuy có dễ dàng nhưng chậm.

+ Dùng command line trên bash (hoặc cmd đối với Windows): Đây là phương thức phổ biến nhất. Ta chỉ cần dùng lệnh để thực hiện các thao tác. Việc thực hiện nhanh và dễ dàng. Phần sử dụng xem ở phần các lệnh trong Github.

## Các dịch vụ sử dụng hệ thống phân tán (Git) được cung cấp:

+ Thông thường chúng ta nhập chung hai khái niệm git và github lại với nhau và hiểu theo cùng một nghĩa. Nhưng Github chỉ là một dịch vụ cung cấp cho người dùng, thông qua Git ta có thể quản lý mã nguồn và lưu trữ trên đó. Ngoài Github còn nhiều trang khác cung cấp dịch vụ như Bitbucket, Google Git, ...

+ Ở đây khuyến nghị sử dụng dịch vụ do Github cung cấp với những lý do sau:

	+ Github khá phổ biến.

	+ Github hoàn toàn miễn phí (nhưng các project miễn phí sẽ public).

	+ Cộng động Open Source hiện đang dùng Github phát triển cũng như lưu trữ dự án. Ta dễ dàng tìm được những project cũng như những thứ cần thiết cho quá trình phát triển dự án để tham khảo.

## Cấu trúc của Git:

+ Tham khảo ở https://en.wikipedia.org/wiki/Git. Phần này mọi người có thể đọc để hiểu rõ chi tiết.

+ Cách dùng Git cơ bản:
	1. **Tạo một Repository:** Để tạo một local repo (trên máy tính cá nhân) mới ta chỉ cần tạo một thư mục mới sau đó vào thư mục này (trên command line) gõ lệnh git init.
	2. **Checkout một Repository:** Để tạo một bản sao chép local repo trên mạng về máy ta thực hiện lệnh:
	
		```git
		git clone /path/to/repo.
		```
		
		+ Nếu sử dụng một máy chủ từ xa dùng lệnh:
		
		```git
		git clone username@host: /path/to/repo.
		```
		
	3. **Workflow:**  Trong một local repo trên máy tính cá nhân sẽ bao gồm 3 cây được duy trì bởi .git
		+ Đầu tiên là Working Directory giữ các file thuộc project.

		+ Thứ hai là Index: hoạt động như một thư mục trung gian trước khi ta đẩy lên.

		+ Cuối cùng là HEAD: chỉ đến cam kết cuối cùng mà bạn đã thực hiện.

		![logo](https://github.com/truongthanhdat/MyDocumentations/blob/master/images/Workflow.png)
		
	4. **Add và commit:**
	
		+ Chúng ta có thể xuất thay đổi đến Index thông qua lệnh:

		```git
		git add <file name>
		git add *
		git add .
		```
		
		+ Đây là một trong những bước cơ bản đầu tiên trong hệ thống làm việc của git. Nếu bạn đã chắc chắn giao thác những thay đổi đến HEAD, ta thực hiện lệnh:
		
		```git
		git commit -m "Commit message"
		```
		
		+ Bây giờ file đã được giao thác đến HEAD, nhưng vẫn chưa được đưa lên repository trên cloud.

	5. **Pushing changes:**
		
		+ Những thay đổi của bạn hiện đang nằm ở HEAD trong thư mục local repository. Để gửi những thay đổi này đến thư mục cloud repository, ta thực hiện lệnh:
		
		```git
		git push orgin master
		```
		
		+ Thay đổi master đến nhánh mà bạn muốn đẩy những thay đổi ở head lên (mặc định của một repository có tên remote là origin và nhánh là master).

		+ Nếu bạn không có clone một một repository có sẵn về local và muốn kết nối kho git của bạn đến repository trên cloud, bạn thực hiện lệnh:
		```git
			git remote add origin <server>
		```
		
		+ Bây giờ bạn có thể đẩy những thay đổi của mình lên repository trên cloud.

	6. **Nhánh (Branching):**

		+ 

	
