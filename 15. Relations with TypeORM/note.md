- Tạo Entity với TypeORM -> Tự động tạo Repository

- Sử dụng ManyToOne => TypeORM tự động thêm một trường khóa ngoại vào Table

- user.reports cho phép truy cập vào tất cả những Report thuộc về User đó
- Report không tự động được fetch khi fetch User

- @OneToMany(() => Report, (report) => report.user)
  => Tham số thứ nhất cho biết User liên kết với Record thuộc kiểu Report. Sử dụng Function để đảm bảo các Entity tại đã được định nghĩa và tránh liên kết tới undefined, một vấn đề thường xảy ra với Circular Dependency (A liên kết với B, B cũng liên kết với A)

- Khi một Report được tạo, cần thêm một User Entity Instance vào trường user của Report Entity Instance đó. Nhưng behind-the-scence thì save Method của Repository sẽ trích xuất id của User Entity Instance và chỉ lưu trữ id đó trong trường user của Report Record trong Database

- Thông thường sẽ không trả về Embedded Object trong Response, mà chỉ trả về id của Record mà trường thông tin đó tham chiếu đến
