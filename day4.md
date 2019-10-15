Resource Manager
- Quản lý tài nguyên (giống tủ rack)
- Khóa, chuyển, xóa Resource Group
Terminology

- Role-based Access Control
	- Quản lý tài nguyên
	- Phân quyền tài nguyên

Day 4 Tạo và quản lý tài khoản, lưu trữ trên azure

- Azure Storage: Lưu trữ tệp, tin nhắn, bảng và các loại thông tin khác
- Lưu trữ bền vững, an toàn, quản lý và truy cập dễ dàng
- Quản lý với nhiều tài khoản
- Các loại:
	- Máy ảo: Ổ đĩa, file shares
	- Dữ liệu phi cấu trúc: Blob, data lake
	- Cấu trúc: Bảng, Cosmos DB, Azure SQL DB

- Các loại Storage file:
	- Blobs: Lưu trữ văn bản, nhị phân, các loại có thể mở rộng, image, video
	- Azure File: Lưu trữ file share cho mô hình on-primes
	- Azure Table: NoSQL
	- Azure Queues: Lưu trữ các tin nhắn truy vấn dữ liệu
	** Chưa phân quyền được
- 2 Dạng Storage Accounts:
	- Standard:
		- Backed by magnetic drives (HDD)
		- Lowest cost per GB, tính theo thực tế dung lượng sử dụng
	- Premium:
		- Backed by solid state drives (SSD)
		- Chỉ sử dụng cho VM disk 
		- Chi phí cao, tính toàn bộ dung lượng ổ đĩa
	- IOPS: Check link
	https://docs.microsoft.com/en-us/azure/virtual-machines/windows/disks-types
	
- Storage Types:
	- Storage V2: Version mới nhất, giá thấp, support mọi file

- Accessing Storage	
	- Blob: http://mystorage**.blob.core.windows.net
	- Table: http://mystorage**.table.core.windows.net
	- Queue: http://mystorage**.queue.core.windows.net
	- File Service: http
	- Sử dụng Domain Server tạo bản ghi CName: để lưu lại domain khác
- Azure Storage Explore: 
download: https://azure.microsoft.com/en-us/features/storage-explorer/
	- Truy cập từ nhiều tài khoản với nhiều subcription
	- Tạo, xóa, xem, sửa storage resource
	- Xem, sửa Blob, Queue, Table,File, Cooss DB, Data lake
	- Share theo access keys, 
		- Có loại sẽ exprie
- Storage Explore Connection Options
	- Kết nối đến Azure subcription
	- Làm việc như local storage
	- Attach to external storage
	- Attach a storage account
	
- Blob storage overview
	- Blob Storage: Lưu dữ liệu phi cấu trúc, lưu văn bản, và nhị phân
	- Blob Containers:
		- Mục đích: Lưu trữ như container service
		- Phân quyền: 
				- Private: không cho phép ai truy cập
				- Blob Access: Cho phép mọi người có quyền chỉ đọc
				- Container access: Cho phép mọi người đọc, lisst entire container, bao gồm cả blobs
				
	- Blob performance Tiers
		- Hot tier (inferred): Dành cho loại dữ liệu truy cập thường xuyên
		- Cool Tier: data không thường xuyên (ít nhất 30 ngày)
		- Archive: 180 days
		- Letancy của Archive sẽ thấp nhất, Hot tier sẽ cao nhất.
	- Uploading Blobs:
		- Block Blobs: Text, binary files
		- Page blob: for frequent read/write
		- 
	
		** Mục đích: Lưu dữ liệu phi cấu trúc, văn bản, video. **
		** Lưu data file, log file, hình ảnh **
		** Backup dữ liệu, khôi phục **
		** Có thể cho lưu trữ trên on-premises hoặc Azure hosted service *




	- Blob Access Policy
	- Blob Pricing
			- File Share: 0.06/GB per month
			- Block Blobs: 0.0002/GB month
		- Storage cost
		- Blob storage
		- Data access
		- Transactions (số lượt truy nhập)
		- Cost dựa trên từng regions
		- Outbound data: tính phí
		- Changing the storage tier: tính phí
- Auzre File Overview
	- Auzre File: có thể map như network drives
	- So sánh Files và Blobs
	- Tạo file shares
	- Map với Windows
	- Map với Linux
	- Chuyển dữ liệu an toàn
	- Tạp Snapshots : giới hạn 200 snapshot 1 ngày, dung lượng 5TB tối đa
	- Backup Azure file
	- Chi phí bằng dung lượng lưu trữ, snap 
	
	Mục đích
	- Share file theo chuẩn SMB 3.0
	- Thay thế và bổ sung dữ liệu
	- Lift and shift
	- Azure File Sync: Backup 1 con server file lên azure (đồng bộ file server)
	- Shared applications
	- Diagnostic data
	- Tools and utilities
So sánh File vs Blobs
File: 
- Sử dụng theo SMB, lưu trữ dữ liệu từ xa
- Truy cập trực tiếp từ mọi nơi, 
- REST interface that allows access from anywhere to stored files.
- Lift and shift, map vào nhiều máy ảo, 
- Có thể kết nối nhiều máy ảo, máy thật, đồng thời
- Có công cụ phát triển
- Maximum connection: 
- tối đa 250 file storage
Blob: 
- dùng như máy chủ dữ liệu phi cấu trúc,	
- support streaming and random-access
- access application data from anywhere

Creating file share:

- Bảo đảm port 445 được mở cho SMB
- Secure Transfer Required (mặc định bật))

- File snapshot: chụp lại thời điểm snapshot, không cho phép chỉnh sửa
	- Chống lỗi dữ liệu, 
	- Bảo vệ chống xóa, thay đổi ngoài ý muốn
	- Backup thông thường

