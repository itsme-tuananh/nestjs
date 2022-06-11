- Service: Nơi đặt Business Logic và fetch Data from Repository
- Repository: Nơi lưu trữ Storage-Related Logic

- Khi throw Exception trong Request Handler, Nest sẽ tự động handle trả về Response ngay tại thời điểm đó

- Dependency Injection Container Flow

* Bắt đầu, register tất cả Class với Container
* Container sẽ phân tích mỗi Class cần Dependency nào
* Khi cần, sẽ yêu cầu Container tạo Instance của một Class (thường là tạo Controller)
* Container sẽ tạo tất cả Dependency cần thiết và trả về Instance của Class
* Container sẽ lưu trữ những Instance đã được tạo của các Dependency và tái sử dụng nếu cần thiết

- Provider: Những thứ có thể được sử dụng làm Dependency cho những Class khác (tái sử dụng những Instance đã được tạo)

- 'Better Approach' tái sử dụng những Instance của các Dependency đã được tạo và luôn hoạt động dựa trên các Instance cụ thể trong Project. 'Best Approach' sử dụng Interface để có thể tương tác với những Implementation khác nhau của cùng một Dependency
- Mỗi khi một Instance của một Dependency được tạo, Nest sẽ lưu trữ Instance đó để tái sử dụng khi có bất cứ Class nào khác cũng sử dụng Instance đó làm Dependency và Instance đó sẽ được chia sẻ giữa các Class cùng sử dụng nó làm Dependency

- Sử dụng DI giúp cho việc Testing dễ dàng hơn :)))
