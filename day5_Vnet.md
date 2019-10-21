- Share Access Signatures (SAS)
	- Cung cấp quyền truy cập
	- Cấp quyền truy cập cho khách hàng mà k cần chia sẻ tài khoản, chỉ cần key
	- 1 tài khoản SAS có thể truy cập 1 hoặc nhiều hơn các dịch vụ storage
	- Khóa SAS có thể truy cập đủ các dịch vụ Storage
	
- Tạo SAS
	Tạo qua Portal hoặc power shell
- Mã hóa dịch vụ lưu trữ (Encryption)
	- Mã hóa chuẩn 256-bit AES
	- bật cho tất cả các storage account và k thể tắt
	- Người dùng tự quản lý Azure Key Vault
	- Tạo khóa quản lý (managed key) và lưu trữ trong key vault
	Bestpratics: 
		- Dùng HTTPS để tạo và phân phối SAS
		- Tạo policy để truy cập
		- Giới hạn thời gian truy cập SAS
		- Tự gia hạn SAS nếu cần
		- Để ý thời điểm SAS bắt đầu
		- Xác định resource được quyền truy cập
		- Khi đã share storage cho user thì khi đó sẽ mất chi phí nếu người dùng sử dnjg
		- Validate data written using SAS
		- Có tool Storage analytis để theo dõi
		
Virtual Network Overview
- Các dịch	vụ chính
	- Virtual Network
	- Load balancer
	- Azure DNS
	- Application Gateway
	- VPN Gateway
	- ExpressRoute
	- CDN
	- Traffic Manager
	- Network Watcher
IP Addressing
	- Private IP address sử dụng trong Az virtual network (Vnet)
	- Public IP address
- Vnet (có thể sửa được address space sau khi tạo)

- Application Gateway | Front-end configuration : Dynamic IP ok, Static: NA
- VPN Gateway | Gateway IP configuration: Dynamic IP: OK, Static : NA
- Load Balancer: Front-end Configuration: Dynamic IP: ok, Static: OK


- Service Endpoints:
	- GIới hạn quyền truy cập đến subnet và IP address (giống security group)
	- Nâng cao tính bảo mật
	- tạo mất 15 phút
- Secure Access to Storage Endpoints
	- Phải cấu hình cả 2 đầu



	
	
		