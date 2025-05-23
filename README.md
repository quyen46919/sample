### 1. Thuộc tính của thẻ (attribute)

---

Attribute là những từ đặc biệt được sử dụng trong thẻ mở của một phần tử HTML để sửa đổi hành vi hoặc hiển thị của phần tử đó. Chúng cung cấp thông tin bổ sung về phần tử và bao gồm tên và giá trị, được phân tách bằng dấu bằng.

Ví du:
`<img src="logo.png" alt="Logo" width="100" height="50">`

Trong đó bao gồm:

- Thuộc tính bắt buộc (required): `src` - định nghĩa đường dẫn ảnh
- Không bắt buộc (optional): `alt` - định nghĩa chú thích cho ảnh; `width` - `height` định nghĩa chiều rộng - chiều dài của ảnh

### 2. Cách trỏ đường dẫn thư mục

---

`../` Trỏ đến thư mục hiện tại – nơi chứa file cùng cấp.  
`./` Trỏ đến một cấp thư mục phía trên (cha của thư mục hiện tại). Có thể sử dụng nhiều lần để đi lên nhiều cấp.  
`/` Trỏ đến thư mục gốc của hệ thống

```
website/
├── index.html <-- Chúng ta đang ở đây
├── assets/
│   └── images/
│       └── logo.png <-- Cần truy cập đến hình ảnh này
├── css/
│   └── style.css
```

```CSS
background-image: url(./assets/images/logo.png);
```

### 3. Class và ID

---

Dùng `id` khi bạn chỉ cần định danh một phần tử duy nhất  
Mỗi giá trị `id` phải là duy nhất trong một trang HTML (không được trùng)
Tham chiếu bằng dấu # trong CSS hoặc JavaScript.

```HTML
<div id="menu">Nội dung menu</div>
```

```CSS
#menu {
  font-size: 30px;
}
```

Dùng `class` để gán một hoặc nhiều lớp (nhóm) cho phần tử. Cho phép nhiều phần tử chia sẻ cùng một kiểu CSS hoặc event JavaScript.

```HTML
<p class="highlight">Đây là một đoạn văn nổi bật.</p>
<button class="highlight">Đây là một button nổi bật</button>
```

```CSS
#highlight {
  color: red;
}
```

### 4. Thuộc tính CSS cho text

---

### 4.1. Thuộc tính kích thước, khoảng cách

| Thuộc tính                       | Giá trị ví dụ                            | Đơn vị / kiểu giá trị   | Chú thích                                                    |
| -------------------------------- | ---------------------------------------- | ----------------------- | ------------------------------------------------------------ |
| **width**                        | 100px                                    | px, em, rem, %          | Chiều rộng của phần tử                                       |
| **height**                       | 100px                                    | px, em, rem, %          | Chiều cao của phần tử                                        |
| **max-width**                    | 200px                                    | px, em, rem, %          | Chiều rộng tối đa                                            |
| **min-width**                    | 50px                                     | px, em, rem, %          | Chiều rộng tối thiểu                                         |
| **max-height**                   | 200px                                    | px, em, rem, %          | Chiều cao tối đa                                             |
| **min-height**                   | 50px                                     | px, em, rem, %          | Chiều cao tối thiểu                                          |
| **margin**                       | 50px<br>20px 10px<br>10px 20px 30px 40px | px, em, rem, %          | Khoảng cách bên ngoài phần tử                                |
| **margin-right/left/top/right**  | 20px                                     | px, em, rem, %          | Khoảng cách bên ngoài phần tử theo một hướng                 |
| **padding**                      | 50px<br>20px auto<br>10px 20px 30px 40px | px, em, rem, %          | Khoảng cách bên trong (từ viền đến nội dung)                 |
| **padding-right/left/top/right** | 20px                                     | px, em, rem, %          | Khoảng cách bên trong phần tử theo một hướng                 |
| **box-sizing**                   | border-box                               | content-box, border-box | Cách tính tổng kích thước (có tính padding/border hay không) |

### 4.2. Thuộc tính chữ

| Thuộc tính          | Giá trị ví dụ             | Đơn vị / kiểu giá trị                   | Chú thích                                  |
| ------------------- | ------------------------- | --------------------------------------- | ------------------------------------------ |
| **font-size**       | 30px                      | px, em, rem, %                          | Cỡ chữ                                     |
| **font-family**     | 'Seaweed Script', cursive |                                         | Phông chữ                                  |
| **font-weight**     | 700, bold                 | 100–900, normal, bold                   | Độ đậm của chữ                             |
| **font-style**      | italic                    | normal, italic, oblique                 | Kiểu chữ nghiêng                           |
| **text-align**      | center                    | left, right, center, justify            | Căn chỉnh dòng chữ                         |
| **text-decoration** | underline                 | none, underline, line-through, overline | Gạch chân, gạch ngang, gạch giữa           |
| **text-transform**  | uppercase                 | none, uppercase, lowercase, capitalize  | Biến đổi kiểu chữ                          |
| **line-height**     | 1.5                       | số, px, %                               | Khoảng cách giữa các dòng                  |
| **letter-spacing**  | 2px                       | px, em                                  | Khoảng cách giữa các ký tự                 |
| **word-spacing**    | 5px                       | px, em                                  | Khoảng cách giữa các từ                    |
| **white-space**     | nowrap                    | normal, nowrap, pre, break-spaces,..    | Xử lý xuống dòng và khoảng trắng           |
| **text-indent**     | 30px                      | px, em                                  | Thụt đầu dòng                              |
| **direction**       | rtl                       | ltr, rtl                                | Hướng viết (trái sang phải hoặc ngược lại) |
| **writing-mode**    | vertical-rl               | horizontal-tb, vertical-rl,...          | Hướng dòng chữ                             |
| **text-shadow**     | 2px 2px 4px #000          |                                         | Bóng của chữ                               |
| **overflow**        | hidden                    | auto, hidden, scroll,...                | Ẩn phần chữ bị tràn ra ngoài khung         |
| **text-overflow**   | ellipsis                  | clip, ellipsis,...                      | Cách hiển thị khi chữ tràn ra ngoải khối   |

### 4.3. Thuộc tính trang trí

| Thuộc tính                | Giá trị ví dụ                | Đơn vị / kiểu giá trị               | Chú thích                                |
| ------------------------- | ---------------------------- | ----------------------------------- | ---------------------------------------- |
| **color**                 | #ffffff                      | color text, hexa, rgb, hsl          | Màu chữ                                  |
| **background-color**      | #f0f0f0                      | color text, hexa, rgb, hsl          | Màu nền                                  |
| **background-image**      | url("image.jpg")             | url(path)                           | Sử dụng hình ảnh làm nền                 |
| **background-size**       | 200px                        | size, contain, cover                | Kích thước ảnh nền                       |
| **background-repeat**     | no-repeat                    | repeat, no-repeat,...               | Kiểu lặp lại ảnh nền                     |
| **background-position**   | center center                | center, center(x) center(y),...     | Vị trí ảnh nền                           |
| **background-attachment** | fixed                        | scroll, fixed, local                | Nền cuộn hay cố định                     |
| **border**                | 1px solid #000               | kích thước - kiểu - màu             | Viền (dạng tổng quát)                    |
| **border-width**          | 2px                          | px, em                              | Độ dày viền                              |
| **border-style**          | solid                        | solid, dashed, dotted               | Kiểu đường viền                          |
| **border-color**          | #ffffff                      | color text, hexa, rgb, hsl          | Màu đường viền                           |
| **border-radius**         | 50%                          | px, %                               | Bo góc                                   |
| **outline**               | 2px dotted red               | kích thước - kiểu - màu             | Đường viền ngoài (không chiếm diện tích) |
| **box-shadow**            | 2px 2px 10px rgba(0,0,0,0.3) |                                     | Đổ bóng hộp                              |
| **opacity**               | 0.8                          | từ 0 đến 1                          | Độ trong suốt                            |
| **cursor**                | pointer                      | none, pointer, default, not-allowed | Giao diện con trỏ chuột khi hover        |

### 4.4. Display

Thuộc tính display cho phép xác định cách hiển thị của các phần tử HTML theo một cách khác so với cách hiển thị mặc định của chúng.

`display: block` Thiết lập cho một phần tử chiếm diện tích của một hàng (full width), có thể set margin (top left right bottom) và width, height.  
 `display: inline` Thiết lập cho một phần tử chiếm diện tích đủ để chứa phần tử đó, từ đó nhiều phần tử có thể nằm chung một hàng. Không thể set width height, margin top bottom.  
 `display: inline-block` Kết hợp đặc tính của block và inline.  
 `display: none` Ẩn phần tử (kể cả kích thước của nó)

#### Display: flex

Flexbox (Flexible Box Layout) là một dạng hiển thị giúp bạn dễ dàng canh chỉnh các phần tử con theo hàng ngang hoặc dọc và tự động co giãn theo kích thước màn hình.  
Tuy nhiên, flex không được hỗ trợ ở các phiên bản trình duyệt cũ.  
Tham khảo: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

Tổng quan về cấu trúc của Flexbox:  
<img src="https://itviec.com/blog/wp-content/uploads/2024/05/flex-css-vippro.png" alt="flex-direction" width="400"/>

### Thuộc tính cho phần tử cha (flex container)

`flex-direction`: Hướng sắp xếp phần tử con

- **row** (mặc định): từ trái sang phải trong ltr; từ phải sang trái trong rtl
- **column**: giống như hàng nhưng từ trên xuống dưới
- **row-reverse**: ngược chiều với row
- **column-reverse**: ngược chiều với column

<img src="https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg" alt="flex-direction" width="400"/>

`flex-wrap`: Hướng sắp xếp phần tử con

- **nowrap**: tất cả các phần tử con sẽ nằm trên một dòng
- **wrap**: các phần tử con có thể nằm nhiều dòng, từ trên xuống dưới nếu hàng đó không đủ kích thước để chứa.
- **wrap-reverse**: ngược chiều với wrap

<img src="https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg" alt="flex-wrap" width="400"/>

`justify-content`: Căn chỉnh phần tử con trên trục dọc (ngược lại sẽ là trục ngang khi direction: column)

- **flex-start**: phân bổ toàn bộ phần tử về phía bên đầu
- **flex-end**: phân bổ toàn bộ phần tử về phía đuôi
- **center**: phân bổ toàn bộ phần tử vào chính giữa
- **space-between**: phân bổ đều trên một dòng, 2 phần tử bên ngoài sẽ nằm đầu và cuối
- **space-around**: phân bổ đều trên một dòng và khoảng cách giữa các phần tử đều bằng nhau, có khoảng cách ở đầu và cuối
- **space-evenly**: phân bổ sao cho khoảng cách giữa bất kỳ hai phân tử nào (và khoảng cách đến các cạnh) bằng nhau.

<img src="https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg" alt="justify-content" width="400"/>

`align-items`: Căn chỉnh phần tử con trên trục ngang (ngược lại sẽ là trục dọc khi direction: column)

- **stretch**: kéo giãn kích thước của phần tử con để lấp đầy vùng chứa (vẫn đảm bảo min-width/max-width)
- **flex-start**: căn chỉnh toàn bộ phần tử về phía trên
- **flex-end**: căn chỉnh toàn bộ phần tử về phía dưới
- **center**: căn chỉnh phần tử về chính giữa (đều ở 2 phía trên và dưới)
- **baseline**: căn chỉnh toàn bộ phần tử theo đường cơ sở

<img src="https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg" alt="align-itemst" width="400"/>

`align-content`: Căn chỉnh phần tử con dọc theo trục chéo

- **stretch**: Các dòng được kéo giãn để lấp đầy chiều cao khả dụng của flex container trên trục chéo
- **flex-start**: căn chỉnh toàn bộ phần tử về phía trên bên phải
- **flex-end**: căn chỉnh toàn bộ phần tử về phía dưới bên phải
- **center**: căn chỉnh phần tử về chính giữa trung tâm
- **space-between**: tương tự `justify-content: space-between` nhưng theo trục dọc
- **space-around**: tương tự `justify-content: space-around` nhưng theo trục dọc

<img src="https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg" alt="align-items" width="400"/>

### Thuộc tính cho phần tử con (flex items)

`order`: vị trí sắp xếp của phần tử trong flex container

<img src="https://css-tricks.com/wp-content/uploads/2018/10/order.svg" alt="order" width="400"/>

`flex-grow`: xác định phần tử sẽ chiếm bao nhiêu phần trong flex container

Nếu tất cả các phần tử con đều có `flex-grow` là 1, không gian còn lại trong vùng chứa sẽ được phân phối đều cho tất cả.  
Nếu một trong các phần tử con có giá trị là 2, phần tử đó sẽ chiếm gấp đôi không gian so với bất kỳ phần tử con nào khác.

<img src="https://css-tricks.com/wp-content/uploads/2018/10/flex-grow.svg" alt="order" width="400"/>

`flex-shrink`: giảm kích thước của flex item nếu không đủ chỗ trong flex container.

`align-self`: cho phép ghi đè giá trị của align-items cho một flex item cụ thể, cách hoạt động của nó tương tự như thuộc tính align-item.

<img src="https://css-tricks.com/wp-content/uploads/2018/10/align-self.svg" alt="order" width="400"/>

### 4.5. Position

### 4.6. Form

### 4.7. Table

### 4.8. Responsive
