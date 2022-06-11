- DTO không chỉ được sử dụng để định hình dữ liệu vào từ Request, mà còn được sử dụng để định hình dữ liệu ra ở Response

- Interceptor có thể tương tác với Request cũng như Response (tương tự với Middleware)
- Có thể apply Interceptor trên từng Route Handler, tất cả Handler trong Controller, hoặc Global

- implements: Khác extends, sử dụng khi một Class cần thỏa mãn những điều kiện của một Abstract Class hoặc một Interface

- Code trong intercept sẽ được thực thi trước khi Request được handle bởi Request Handler, Code trong map sẽ được thực thi trước khi Response được gửi đi

- User Entity Instance - Interceptor -> User DTO Instance -> JSON

- excludeExtraneousValues: true đảm bảo JSON được trả về chỉ chứa những Property được expose trong DTO

- Behind-the-Scence thì Decorator là Function
