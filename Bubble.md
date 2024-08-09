# **Complete Bubble Developer Course: Build Apps Without Coding**

## 🔷 MỤC LỤC

- **[Tổng quan về Bubble](#tổng-quan-về-bubble)**
- **[Cơ sở dữ liệu](#cơ-sở-dữ-liệu)**
- **[Data View](#data-view)**
- **[Danh sách và truy cập dữ liệu theo code](#danh-sách-và-truy-cập-dữ-liệu-theo-code)**
- **[Giao tiếp giữa các đối tượng](#giao-tiếp-giữa-các-đối-tượng)**
- **[Structured Data Type](#structured-data-type)**
- **[Cập nhật Database](#cập-nhật-database)**
- **[Thiết kế và mô hình hoá màn hình](#thiết-kế-và-mô-hình-hoá-màn-hình)**
- **[Tip](#tip)**

## 🔷Tổng quan về Bubble

### Khái niệm

- **Bubble** là nền tảng NoCode dùng để xây dựng web app mạnh mẽ nhất hiện nay.

Được gọi là Visual Programming Tool (công cụ lập trình trực quan), bạn có thể tạo UI bằng cách kéo thả, setting chi tiết cho từng UI cũng như cách hoạt động của các thành phần, ngoài ra bạn cũng có thể thiết kế database một cách chặt chẽ, từ đó có thể tạo được rất nhiều web service khác nhau.

### Why Bubble?

- **Không cần mã lập trình**: Bubble platform sử dụng nguyên tắc kéo và thả để xây dựng ứng dụng mà không cần viết mã lập trình. Điều này giúp người dùng không cần có kiến thức chuyên sâu về lập trình vẫn có thể tạo ra ứng dụng web chất lượng cao.

- **Tốc độ phát triển nhanh chóng**: Với công cụ kéo và thả trực quan, người dùng có thể nhanh chóng thiết kế giao diện và logic của ứng dụng mà không cần mất nhiều thời gian.

- **Hỗ trợ đa nền tảng**: Bubble platform cho phép người dùng xây dựng ứng dụng web có thể tương thích trên nhiều thiết bị và trình duyệt khác nhau mà không cần phải lo lắng về việc tối ưu hóa giao diện.

- **Mạnh mẽ và linh hoạt**: Bubble cung cấp nhiều tính năng mạnh mẽ như xử lý dữ liệu, tích hợp API, tự động cập nhật dữ liệu và nhiều tính năng khác giúp người dùng xây dựng ứng dụng web đa dạng theo nhu cầu.

- **Cộng đồng hỗ trợ lớn**: Bubble có một cộng đồng người dùng rộng lớn, cùng với tài liệu hướng dẫn phong phú giúp người mới bắt đầu dễ dàng học hỏi và giải quyết vấn đề trong quá trình phát triển ứng dụng.

## 🔷Cơ sở dữ liệu

Bubble sử dụng cơ sở dữ liệu nhúng. Nó kém mạnh mẽ hơn cơ sở dữ liệu SQL của bên thứ ba nhưng cho phép làm việc nhanh chóng.

- **Data Types**
  Cơ sở dữ liệu trong Bubble hoạt động dựa trên "Data Types", tương đương với các bảng trong cơ sở dữ liệu quan hệ. Mỗi "Data Types" đại diện cho một loại đối tượng mà bạn muốn lưu trữ dữ liệu.
  <p align="center" width="100%">
    <img src="images/data-types.png" alt="Data Types">
  </p>

- **Data Fields**
  Đối với mỗi "Data Types", bạn có thể định nghĩa các trường tùy chỉnh. Các trường này được gọi là "Data Fields". Để thêm một "Data Fields", bạn cần nhập tên và chỉ định kiểu dữ liệu của trường đó.
  <p align="center" width="100%">
    <img src="images/data-fields.png" alt="Data Fields">
  </p>

- **App Data**
  Khi bạn đã tạo các loại dữ liệu cần thiết, tất cả chúng có thể được tìm thấy trong tab "App Data", nơi chúng được trình bày dưới dạng bảng. Bạn cũng có thể thêm mới, chỉnh sửa, xóa, export, import dữ liệu ở đó.
  <p align="center" width="100%">
    <img src="images/app-data.png" alt="App Data">
  </p>

- **Option Sets**
  Option Sets là một cách để lưu trữ các tùy chọn (options) hoặc danh sách các mục không thay đổi (static items) mà bạn muốn sử dụng trong ứng dụng của mình. Option Sets giúp bạn quản lý các giá trị cố định một cách dễ dàng và tái sử dụng chúng trong nhiều nơi trong ứng dụng.
  <p align="center" width="100%">
    <img src="images/option-sets.png" alt="Option Sets">
  </p>

- **Relationship**
  Khái niệm "relationship" (mối quan hệ) thường được sử dụng để liên kết giữa các bảng dữ liệu (Data Types) khác nhau trong cơ sở dữ liệu của ứng dụng. Bubble không sử dụng các mối quan hệ cơ sở dữ liệu tiêu chuẩn. Chúng được cấu hình thông qua các loại. Trong Bubble, có một số loại mối quan hệ chính:

  - **One to One Relationship (1-1):** Một phần tử của bảng này chỉ được liên kết với duy nhất một phần tử của bảng khác.
  - **One to Many Relationship (1-N):** Một phần tử của bảng này có thể được liên kết với nhiều phần tử của bảng khác.
  - **Many to Many Relationship (N-N):** Mỗi phần tử trong mỗi bảng có thể được liên kết với nhiều phần tử trong bảng còn lại.
    Ví dụ:
    Bạn có thể tạo một mối quan hệ Many to Many giữa hai Data Types `Product` và `Order` bằng cách sử dụng một Data Type trung gian là `Order Detail`. Mỗi sản phẩm có thể được đặt trong nhiều đơn hàng và mỗi đơn hàng cũng có thể chứa nhiều sản phẩm.

  1. Tạo Data Types `Product`, `Order`, và `Order Detail`.
  2. Thêm trường `Products` kiểu "List of Products" vào Data Type `Order Detail`
  3. Thêm trường `Orders` kiểu "List of Orders" vào Data Type `Product`
  4. Khi hiển thị thông tin của một đơn hàng, bạn có thể truy cập danh sách sản phẩm trong đơn hàng đó thông qua Data Type Order Detail.
