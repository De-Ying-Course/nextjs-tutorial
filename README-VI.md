## Hướng dẫn Next.js

[Chuyển sang tài liệu Tiếng Anh](https://github.com/De-Ying-Course/nextjs-tutorial/blob/main/README.md)

Next.js gần đây đã trở thành khung React chính thức như được nêu trong tài liệu React. Trong khóa học này, bạn sẽ tìm hiểu các khái niệm Next.js quan trọng nhất và cách chúng phù hợp với hệ sinh thái React. Cuối cùng, bạn sẽ kiểm tra kỹ năng của mình bằng cách xây dựng ứng dụng Next 13 toàn ngăn hiện đại.

📚 Trong dự án này, bạn sẽ học:

- Cấu trúc thư mục ứng dụng Next.js 13
- Next.js 13 Thành phần máy khách so với Thành phần máy chủ
- Next.js 13 Định tuyến dựa trên tệp (bao gồm các tuyến động và lồng nhau)
- Trang Next.js 13, bố cục, tải và lỗi Tệp đặc biệt
- Next.js 13 Trình xử lý định tuyến không có máy chủ (API tiếp theo, Ứng dụng ngăn xếp đầy đủ)
- Next.js 13 Siêu dữ liệu và Tối ưu hóa Công cụ Tìm kiếm (SEO)
- Ba cách để tìm nạp dữ liệu trong Next.js:
  - Kết xuất phía máy chủ (SSR),
  - Tạo trang web tĩnh (SSG)
  - Thế hệ tĩnh gia tăng (ISR)

## Nội dung của các phần

### Lợi ích của Next.js

<details>
    <summary><b>Next.js có gì mà React không có?</b></summary>
    <br /><p>+ Next.js đơn giản hóa quá trình phát triển</p>
    <p>+ Ngoài ra, nó còn tối ưu hóa các ứng dụng web của bạn</p>
</details>

<details>
    <summary><b>Khám phá các tính năng của Next.js</b></summary>
    <details>
        <summary><b>Rendering</b></summary>
        <details>
            <summary><b>Hiển thị phía máy khách và phía máy chủ là gì?</b></summary>
            <ul>
                <li>Kết xuất phía máy khách hoặc kết xuất trình duyệt là khi người dùng yêu cầu một trang web, máy chủ sẽ gửi một tài liệu HTML cơ bản và mã JS, trình duyệt sau đó tải xuống và thực thi mã JS dẫn đến kết xuất các thành phần và cuối cùng là hiển thị trang web </li>
                <li>Kết xuất phía máy chủ liên quan đến việc kết xuất trang web trên máy chủ trước khi truyền nó đến thiết bị của khách hàng khi người dùng yêu cầu một trang, máy chủ sẽ xử lý yêu cầu và kết xuất các thành phần ở phía máy chủ, sau đó máy chủ sẽ gửi lại HTML được kết xuất đầy đủ đến trình duyệt của khách hàng cho phép hiển thị ngay lập tức</li>
                <li>Sự khác biệt này làm nổi bật một khía cạnh thiết yếu của SEO Phát triển Web (Tối ưu hóa Công cụ Tìm kiếm)</li>
            </ul>
        </details>
        <details>
            <summary><b>SEO là gì?</b></summary>
            <ul>
                <li>Kết quả là SEO hay còn gọi là trình thu thập thông tin của công cụ tìm kiếm gặp khó khăn khi lập chỉ mục Trang được hiển thị động ở phía máy khách</li>
                <li>Hiệu suất SEO của các trang như vậy có thể bị ảnh hưởng do các công cụ tìm kiếm có thể không hiểu đầy đủ nội dung của chúng và xếp hạng chúng một cách thích hợp bằng cách sử dụng Next.js</li>
                <li>Vấn đề này được giải quyết bằng cách gửi mã kết xuất trước trực tiếp tới máy khách. Việc thu thập thông tin và lập chỉ mục này của các công cụ tìm kiếm giúp cải thiện SEO</li>
            </ul>
        </details>
        <details>
            <summary><b>Tại sao tôi nên ưu tiên SEO?</b></summary>
             <ul>
                <li>SEO rất quan trọng để tối ưu hóa khả năng hiển thị và xếp hạng của trang web trong kết quả của công cụ tìm kiếm bằng cách tập trung vào SEO</li>
                <li>Bạn có thể đạt được một số lợi ích, bao gồm: lưu lượng truy cập không phải trả tiền tăng lên, trải nghiệm người dùng nâng cao, uy tín và độ tin cậy, lợi thế cạnh tranh do xếp hạng kết quả tìm kiếm cao hơn</li>
                <li>Việc ưu tiên SEO có thể tác động lớn đến sự thành công của trang web của bạn và sự hiện diện trực tuyến của trang web đó </li>
            </ul>
        </details>
    </details>
    <details>
        <summary><b>Routing</b></summary>
         <details>
                <summary><b>Làm cách nào để tạo các tuyến trang khác nhau trong React?</b></summary>
                <ul>
                   <li>Chúng ta phải cài đặt một gói bổ sung có tên là react-router-dom và sau đó tạo các tuyến đường trong một trong các tệp</li>
               </ul>
          </details>
          <details>
              <summary><b>Vậy làm thế nào để bạn tạo các tuyến đường trong Next.js?</b></summary>
               <ul>
                   <li>Next.js sử dụng hệ thống định tuyến dựa trên tệp Điều đó có nghĩa là việc định tuyến được xử lý bởi hệ thống tệp, mỗi thư mục trong thư mục ứng dụng sẽ trở thành một tuyến đường và tên thư mục sẽ trở thành đường dẫn tuyến đường, ví dụ: nếu bạn có một thư mục có tên trong thư mục mà bạn có thể truy cập các trang đó ở dấu gạch chéo về phía trước của đường dẫn không dễ dàng như vậy</li>
                    <li>Không cần các gói bên ngoài hoặc cấu hình phức tạp</li>
                 <li>Bạn có thể tạo tệp cho các tuyến đường mình muốn và mở chúng ngay lập tức trong ứng dụng của mình</li>
               </ul>
          </details>
      </details>
      <details>
        <summary><b>Fullstack</b></summary>
        <details>
              <summary><b>API Routes</b></summary>
               <ul>
                   <li>Cho phép tạo các hàm serverless để xử lý các yêu cầu API</li>
                   <li>API Serverless trong Next.js là một cách tạo điểm cuối API</li>
                   <li>Không cần máy chủ truyền thống</li>
                   <li>Nó cho phép chúng tôi xây dựng và triển khai API: mà không cần quản lý cơ sở hạ tầng máy chủ, không phải lo lắng về việc mở rộng quy mô máy chủ của họ khi lưu lượng truy cập tăng lên</li>
                   <li>Với tính năng này, chúng tôi có thể tạo các điểm cuối API bằng cách chỉ cần tạo một tệp có tên route.js trong một thư mục cụ thể trong thư mục ứng dụng. Tệp này trong bất kỳ đoạn tuyến nào của ứng dụng lại tương ứng trực tiếp với điểm cuối API tuyến đó</li >
               </ul>
          </details>
          <details>
              <summary><b>Automatic Code Splitting</b></summary>
               <ul>
                   <li>Tách mã là một kỹ thuật chia nhỏ các gói mã JavaScript lớn thành các đoạn mã nhỏ hơn, dễ quản lý hơn để có thể tải khi cần</li>
                   <li>Khi cần, điều này giúp giảm thời gian tải ban đầu của trang web và tối ưu hóa trải nghiệm của người dùng khi duyệt</li>
                   <li>Chúng tôi phải thực hiện nhiều cấu hình khi ứng dụng của bạn phát triển</li>
                 <li>Theo mặc định, nó sử dụng phân tách mã tự động để chia các trang thành các phần riêng biệt khi người dùng điều hướng đến một trang khác, chỉ mã cần thiết cho trang đó được tải dẫn đến điều hướng trang tiếp theo nhanh hơn </li>
               </ul>
          </details>
        <details>
              <summary><b>Vậy, bài học rút ra là gì?</b></summary>
               <ul>
                   <li>Phát triển giao diện người dùng đã trải qua nhiều tiến bộ khác nhau: linting, định dạng, biên dịch, đóng gói, thu nhỏ, triển khai</li>
                   <li>Để họ tập trung vào mã thực tế, đó là nơi Next.js phát huy tác dụng: tự động hóa hầu hết các quy trình còn lại và cho phép chúng tôi tập trung vào việc xây dựng logic nghiệp vụ thiết yếu của ứng dụng</li>
               </ul>
          </details>
        <details>
              <summary><b>Vẫn chỉ là React thôi</b></summary>
               <ul>
                   <li>Next.js không phải là một công nghệ hoàn toàn mới</li>
                   <li>Về cơ bản, nó vẫn được xây dựng dựa trên React</li>
                   <li>Mục đích của nó là đơn giản hóa một số tác vụ nhất định cho phép các nhà phát triển tập trung vào mã React cốt lõi</li>
               </ul>
          </details>
      </details>
</details>

### Cấu trúc tệp & thư mục

![img](https://i.imgur.com/YBQQ0DV.png)

```
Ứng dụng >
    layout.js >
        - Mọi mã được viết trong tệp này sẽ được hiển thị trên mọi tuyến trang bạn tạo
        - Tệp duy nhất này cho phép bạn cá nhân hóa hành vi của ứng dụng bằng cách cung cấp bố cục hoặc mẫu chung cho tất cả các trang, bất kỳ thành phần nào bạn đưa vào tệp này sẽ được chia sẻ trong toàn bộ ứng dụng của bạn
        - Ngoài ra, tệp bố cục cũng cho phép bạn tùy chỉnh giao diện của tài liệu HTML để bạn có thể đặt những thứ như ngôn ngữ và bạn cũng có thể sửa đổi siêu dữ liệu cho tất cả các trang
    page.js >
        - Đại diện cho lộ trình trang chủ của ứng dụng IE
    globals.css >
        - Chứa kiểu CSS toàn cầu của toàn bộ ứng dụng
```

### Thành phần Máy khách & Máy chủ

1. Những cách mới để hiển thị các thành phần của bạn

![img](https://i.imgur.com/aBpUKWh.png)

- Theo mặc định, tất cả các thành phần được tạo Next.js trong thư mục ứng dụng là các thành phần máy chủ phản ứng
- Điều đó có nghĩa là Next.js tận dụng kết xuất phía máy chủ để nâng cao tốc độ tải trang ban đầu dẫn đến SEO và trải nghiệm người dùng được cải thiện ngay bây giờ trong trường hợp bạn muốn biến thành phần phía máy chủ đó theo mặc định thành phía máy khách mà bạn cần thêm chỉ thị 'sử dụng ứng dụng khách' ở đầu trang của bạn để biến nó thành thành phần phía máy khách bằng cách sử dụng cả thành phần máy khách và thành phần máy chủ cho phép chúng tôi tận dụng các lợi ích của kết xuất phía máy chủ trong khi vẫn sử dụng khả năng phản ứng để xây dựng Động và giao diện người dùng tương tác

2. Khi nào nên sử dụng Thành phần Máy chủ và Máy khách

![img](https://i.imgur.com/3uebcX4.png)

### Định tuyến & Tệp Next.js Đặc biệt

1. Định tuyến dựa trên thư mục

![img](https://i.imgur.com/kqgySIK.png)

2. Định tuyến động

![img](https://i.imgur.com/glwoZ32.png)

### Đang tìm nạp dữ liệu

1. Server Side Rendering (SSR)

- Điều đó có nghĩa là dữ liệu kết xuất của máy chủ Động được tải mới trên mỗi yêu cầu với SSR, mỗi yêu cầu đến máy chủ sẽ kích hoạt một chu kỳ kết xuất mới và tìm nạp dữ liệu để đảm bảo rằng nội dung luôn được cập nhật tại đây
- Bộ nhớ cache: 'no-store' nó chỉ đơn giản có nghĩa là này, đừng lưu trữ nó, chỉ cần gọi nó và sau đó hiển thị 'tiêu đề và nội dung' của bài đăng đã tìm nạp, điều này sẽ đảm bảo rằng nó sẽ tải lại nó mỗi lần. Điều đó có nghĩa là nó phía máy chủ được hiển thị ngay bây giờ để chuyển sang ví dụ thứ hai của chúng tôi Đó là thế hệ tĩnh, điều duy nhất chúng tôi phải làm là loại bỏ tiền mặt này không có cửa hàng.

2. Static Site Generation (SSG)

- Điều đó có nghĩa là mặc định Next.js sử dụng Static Site Generation
- Nó sẽ tự động lấy dữ liệu này ngay tại đây nhưng nó cũng sẽ lưu vào bộ đệm ẩn phương pháp này là ý tưởng cho Nội dung không thay đổi thường xuyên

3. Incremental Static Regeneration (ISR)

- Nó kết hợp các lợi ích của SSR và SSG cho nội dung động trong các trang web tĩnh với Tái tạo tĩnh gia tăng, bạn có thể chỉ định một số dữ liệu nhất định sẽ được tìm nạp tĩnh tại thời điểm xây dựng trong khi xác định khoảng thời gian xác thực lại, điều này có nghĩa là dữ liệu sẽ được lưu vào bộ nhớ cache nhưng sau một thời gian cụ thể frame, sau đó, nó sẽ làm mới nó và bạn sẽ luôn có dữ liệu mới làm cho điều này trở thành Điều tốt nhất của cả hai thế giới cho nội dung Động
- Next.js cho phép các ứng dụng ở dạng full-stack, nghĩa là chạy ứng dụng cả trên giao diện người dùng và trên phần phụ trợ bằng cách sử dụng cùng một hệ thống định tuyến dựa trên tệp.
- Next.js cho phép chúng tôi xử lý các yêu cầu HTTP và phát triển chức năng back-end mà không yêu cầu máy chủ bên ngoài

### Điểm cuối API Next.js

- Cần lưu ý rằng có hai cách khác nhau để xác định Trình xử lý vòng, cách thứ nhất là tạo trình xử lý định tuyến dựa trên tệp ngay trong thư mục API trong thư mục ứng dụng và cách tiếp cận thứ hai là tạo Trình xử lý định tuyến trực tiếp trong thư mục ứng dụng chính nó
- Bạn sẽ không thể có một tuyến đường trong các bài đăng bên cạnh trang vì Next.js sẽ không biết đây có phải là trang giao diện người dùng thông thường hay tuyến đường API phụ trợ không
- Sẽ xung đột giữa các bài đăng gạch chéo chuyển tiếp sẽ hiển thị một trang thông thường và các bài đăng gạch chéo chuyển tiếp sẽ là một API

![img](https://i.imgur.com/FxGi0EM.png)

- Tôi vẫn đề xuất cách tiếp cận đầu tiên là tạo các tuyến API, nghĩa là không tạo các tuyến ngay trong thư mục ứng dụng thay vì giữ cho mã của chúng ta rõ ràng và dễ hiểu
- Nó cho phép chúng tôi tạo các tuyến phụ trợ đó ngay lập tức next.js hỗ trợ các phương thức HTTP sau:

![img](https://i.imgur.com/1dl4ZYl.png)

### SEO & Siêu dữ liệu

1. Siêu dữ liệu tĩnh (Static Metadata)

![img](https://i.imgur.com/gwaWFSi.png)

2. Siêu dữ liệu động (Dynamic Metadata)

![img](https://i.imgur.com/wfG42af.png)
