# Maintenance vs. Downtime

- Unplanned hardware maintenance -> Action: Live migration
- Unexpected Downtime
- Plan maintenance

# Availability Sets
- Nhiều hơn 2 instance in two or more availibility zones = 99.99% uptime
- Có thể tạo nhiều máy ảo trong availibility set
- có thể tạo app theo từng availibility set
- Update domains: (giống tủ rack) Tên miền cho phép gia tăng, triển khai, có thể phải khởi động lại
- Fault domain: là 1 nhóm máy ảo nằm trên nhiều máy chủ vật lý khác nhau. Ít nhất trong 1 availibilityset sẽ có 2 fault domain

# Scale Sets
## Implementing scale sets
- chọn đc số máy ảo có thể scale lên 100 
- Insance size
## Autoscal
- Tự động điều chỉnh
- Scale out 
- Scale in
- lên lịch được sự kiện tăng giảm
- Giám sát được 
## Implementing autoscale
- dựa trên CPU rồi tăng số lượng VM theo tùy chỉnh

## Virtual Machine Extensions

## Customer Script Extensions

##