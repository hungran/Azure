#Data Protection

## Data Replication Overview

- Replication Options
	- đảm sao lưu, tính sẵn sàng cao
	- 
- Locally-redundant Storage
	- Low-cost
	- Maintains 3 bản ciopy trong  1 nc
	- Tất cả bản sao đều nằm trong khu vực
	- Sư dụng cho trường hop recnstructed
	- Sử dụng cho vùng lãnh thổ
	- Not Available for all
	
- Zone-redundant Storage
	- 3 bản ở 3 zone khác nhau
	- không phải tất cả các region, tuỳ zone có availability mới có tính năng này
	- 
- Geo-redundant Storage
	- Lưu trữ dự phòng theo địa lý
	- 6 bản backup
	- sap chép 3 lần trong khu vực
	- sao chép sang các vùng địa lý  hoặc vùng thứ cấp
	- RTO (recovery time object) : thời gian backup, thời gian tối thiểu phục hồi
	- RPO (: 
- Comparing Replication Strategies
## Backup Component Comparision
- Azure Backup (Mars) agent: Bảo vệ file and foldr, không support Linux
- Azure Backup Server: 
	- Snapshot
	- 
	