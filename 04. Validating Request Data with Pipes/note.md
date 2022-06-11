- Validation Pipe chỉ chạy trên những Route có Validation Rule

- DTO (Data Transfer Object): Mô tả khuôn dạng của Request, có nhiệm vụ vận chuyển dữ liệu, thường không có Functionaliy mà chỉ là những Class đơn giản với những Property khác nhau mà Request Body nên có

- class-transformer: Chuyển Plain (Literal) Object sang Class (Constructor) Object (Instance of a Class)
- class-validator: Xử lí Validation trên Property của Instance của một Class sử dụng Decorator

- Validation Pipe's Work Flow

* class-transformer chuyển Request Body thành một Instance của DTO Class (Plain JSON -> Instance of DTO Class)
* class-validator validate Instance (sử dụng Decorator)
* Nếu có Validation Error, phản hồi ngay lập tức, nếu không sẽ đưa Request Body tới Request Handler

- Tại sao Nest biết phải chuyển JSON từ Request Body thành Instance của DTO Class (bởi TS Code sẽ được compile thành JS Code và mọi thông tin về Type sẽ bị mất)
  -> emitDecoratorMetadata: true sẽ giữ lại một chút thông tin về Type khi TS Code được compile sang JS Code
