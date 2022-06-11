- create: Tạo Entity Instance
- save: Lưu trữ Entity Instance vào Database

- Khi gọi create, Hook được thực thi. Khi chỉ gọi save với Literal Object, Hook không được thực thi

- remove tương tự với save khi Hook được thực thi

- save và remove làm việc với Entity Instance; insert, update và delete làm việc với Plain Object

- Object.assign(): Cập nhật một số trường của Object

- Mọi phần của URL đều là string

- Sử dụng HTTP-Specific Exception trong Service khiến việc tái sử dụng với những Controller sử dụng giao thức khác khó khăn hơn
