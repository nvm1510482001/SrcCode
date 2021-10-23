## BlockChain Research
	
### 1. Smart Contract
### *Đ/n:*
- ***Smart Contract*** Hợp đồng thông minh)* là bộ giao thức đặc biệt tự động thực hiện điều khoản và các thỏa thuận giữa các bên trong hợp đồng nhờ sự hỗ trợ của công nghệ Blockchain
- Được thực hiện tự động, không có sự can thiệp của bên thứ 3
- Minh bạch, có thể dễ dàng truy xuất, không thể bị can thiệp, sửa đổi
- Tương đương một hợp đồng pháp lý và được ghi lại dưới ngôn ngữ lập trình
### *Cách thức hoạt động*:
- Thường tuân theo các câu lệnh “If .... else …”
- Các hợp đồng được quản lý, thực thi khi người dùng (địa chỉ) tương tác với nhau
- Một hợp đồng bao gồm mã hợp đồng và khóa công khai.
	+ Khóa công khai thứ nhất do người tạo hợp đồng cung cấp
	+ Khóa còn lại đại diện cho hợp đồng, và có tính duy nhất
### *Tạo một Smart Contract cần:*
- Chủ thể hợp đồng: Smart Contract cần được cấp khả năng cho phép truy cập vào dịch vụ/ sản phẩm
- Chữ ký điện tử
- Điều khoản hợp đồng
- Nền tảng phân quyền

##2. Solidity
- Code thuộc về contract tương tự với class bên java, ngoài ra còn có interface và library
- Biến trong solirity chia làm 3 loại:
	+ State variables: được lưu trữ vĩnh viễn trong toàn bộ hợp đồng
	+ Local variables:  có giá trị khi hàm được thực thi
	+ Global variables: tồn tại để lấy thông tin từ blockchain chẳng hạn như msg.datadata để gọi data hoàn chỉnh, msg.sender để lấy địa chỉ người gửi, v.v
- Struct và array:
	+ Struct cho phép tạo nhiều cấu trúc data hơn. Ví dụ
        ```solidity
  		struct Developer {
			string name;
			uint data;
		}
		```
	+ Array có thể tạo cố định hay linh hoạt tùy ý. Ví dụ
		+ Developer[] public developers; (mảng linh hoạt)
		+ Deveoper[2] public developers; (mảng cố định)
- Function
	+ Để tạo ra một hàm ta dùng từ khóa `function`. Các fuction mặc định là public
	+ Để định dạng một fuction return ta phải dùng từ khóa `returns`. Ví dụ:
	
	```solidity
	function tshirtCostirtCost(string name) public returns (uint)  
	//trong hàm này giá trị trả về là kiểu uint
	```

    + Ngoài ra ở function còn 1 số từ khóa:
      + `view` nghĩa là function cần xem một vài biến của Contract, mà không được thay đổi nó
      + `pure` nghĩa là function không truy cập vào bất kì data trong contract
+ Có thể tạo các event để có thể tương tác với những gì diễn ra trên blockchain và show trên front end bằng từ khóa `event`