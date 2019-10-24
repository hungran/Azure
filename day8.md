# Virtual Machine Planning
## IaaS cloud serivce
- Test and development
- Website hosting
- Storage, backup, and recovery
- Web apps
- High-performance computing
- Big data analysis

## Planning Checklist
- Start with the network
- Name the VM
- Decide the location for the VM
- Determine the size of the VM
- Understand the pricing model
- Consider storage for the VM
- Select an operating system
## Location and Pricing
### Location
- Có 54 regions trên 140 quốc gia
- Đặt vm gần nhất có thể cho users
- Khả năng cung ứng phần cứng ở mỗi regions lại khác biệt (size của VM)
- Giá của Vm chưa bao gồm ổ cứng của hệ điều hành
- Tính phí hệ điều hành cả khi không dùng máy
- Vị trí máy ảo phải phù hợp với pháp lý hoặc chính sách 
### Pricing
- Sử dụng trang azure calculator để lên dự toán
- managed disk tính theo lưu lượng sử dụng (standard tính theo lượng thực tế dùn, tính theo toàn bộ phana vùng)g)
- Static Ip 1 giá, Dynamic Ip 1 giá (giá khác nhau mỗi vùng, giá có thay đổi liên tục)
- Outbound Data transfer tính theo dung lượng GB có giá khác nhau
- Có license ở on-prem thì giảm đc 40% giá license

## Virtual Machine Sizing
- Gợi ý Sizing như hình dưới
<img src="https://imgur.com/P4GlfLl.jpg">
## Virtual Machine Disks

## Storage Options

## Support Operating Systems
