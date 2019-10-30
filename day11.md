# Network Traffic Management

## System Routes
	- Do Azure đã khởi tạo sẵn
	- Traffice giữa VMs trong cùng subnet
	- ...
## User Defined Routes
	- Tự xác định, định tuyến traffice theo mong muốn
	- Nexthop có t hể là virtual network gateway, virtual netwwork...
	
## Routing Examples
	- Create a routing table
	- Create a
## Create a Routing Table
	- Hỗ trợ BGP (nếu enable)
	- khi bật BGP thì route table tự động add tất cẩ subnet con
## Create a Custome Routes
	- Lưu ý khi chọn nexthop:
		- Virtual network GW, VMnet, intenet or None
		

## Associate the Routes

# Azure Load Balancer Overview

## Azure Load Balancer 

## Public Load Balancer
	- Map Public IP add đến Private VMnet
	- Phân phối, phân tải dịch vụ
## Internal Load Balancer
	- xem slide
	- Cân bằng tải trong mạng ảo private
	- Kết nối chéo (vd nhiều VM nối với nhiều SQL)
## Load Balancer SKUs
	- SKUs are note mutable (không thay đổi đc)
	- LB rule cannot span two virtual networks
	- no charge for the basic LB
	- LB frontends không cho phép kết nối chéo với global virtual network peering
## Backend Pool
	- Phân phối lưu lượng, đến nhóm địa chỉ
	- Basic SKU: VM in a single availability set hoặc VM scale set
	- Standard SKU: Any VM in a single virtual network, including a blend of VMs, availability sets, and VM scale sets.
	
	