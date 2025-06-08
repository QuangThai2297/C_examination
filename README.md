# Kiểm tra năng lực lập trình ngôn ngữ C

## 1. Tin học và máy tính

### 1.1. Đổi dãy nhị phân sau ra hexa
```
00111010 01111111 11000101 00000001 00101110
10101011 10011101 01001111 01101011 10001110
```
Kết quả
```

```
### 1.2. Biểu diễn số nguyên
#### a. Sử dụng 8/16/32 bit để biểu diễn dải số nguyên sau đây (điền các vị trí còn lại)

|  | <div style="width:100px">8 bit </div>| <div style="width:100px">16 bit </div>| <div style="width:100px">32 bit </div>|
|---|---|---|---|
| Không dấu | 0 -> 255 | | |
| Có dấu (dạng bù 2) | | | |

Ví dụ: 8 bit biểu diễn số nguyên không dấu: `0 -> 255 (hoặc 0 -> 2^8 - 1)`, 1 trong 2 cách đều chấp nhận

#### b. Biểu diễn số -5 dưới dạng mã hex 1 byte và dưới dạng mã hex 4 byte

```

```

### 1.3. Biểu diễn kí tự
Theo bảng mã ascii, mã `0x30` biểu diễn kí tự ‘0’

`0x39` biểu diễn kí tự nào?
```
```

## 2. Lập trình C

### 2.1. Kiểu dữ liệu
#### a. Viết câu lệnh lấy kích thước của biến hoặc kiểu dữ liệu sau:
```c
int a = 10;
```
```
```
#### b. Kích thước con trỏ trong vi điều khiển là bao nhiêu
```
```



#### c. Kích thước của struct sau là bao nhiêu:
```c
typedef struct {
    uint8_t member1;
    uint32_t member3;
    uint16_t member2;
} st_t;
```
```
```

### 2.2. Macro
#### a. Macro set,get,clear bit thứ k trong byte n

•   SET_BIT(n, k)
```
```
•   GET_BIT(n, k)
```
```
•   CLEAR_BIT(n, k)
```
```
#### b. Macro trả về giá trị lớn hơn giữa hai số a và b.
    MAX(a, b)
```
```
#### c.	Macro tính bình phương của số x.
    SQUARE(x)
```    
```

### 2.3. Ép kiểu
#### a. Cho đoạn chương trình
```c
uint32_t a = 1;
uint32_t b = 2;
if(a - b > 0)  
    printf("true: 0x%x ", a - b);
else 
    printf("false 0x%x ", a - b);
```
In ra kết quả sau khi chạy
```
```
#### b. Thay đầu vào của chương trình bên trên bằng
```c
int32_t a = 1;
int32_t b = 2;
```
In ra kết quả
```
```

### 2.4. Mảng và con trỏ
#### a. Size 
Kích thước của các mảng dưới đây là bao nhiêu
```c
int array[3] = {1, 2};
int array1[] = {1, 2, 3};
```
Kết quả
```
```

Cho function và câu lệnh gọi funtion bên dưới (với array1 là mảng ở bên trên), 
```c
void show_array(int * array) {
    printf("%d", sizeof(array));
}	
show_array(array1);
```
In ra kết quả sau khi gọi function
```
```

#### b. Mảng 2 chiều (điền kết quả sau dấu =)
```c
int array[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
*((int*)array + 1) = 
```

#### c. Cho (điền kết quả sau dấu =)
```c
uint8_t array[6] = {1, 2, 3, 4, 5, 6};
```
kết quả dạng hexa của
```c
*(uint16_t*)array = 
*(int32_t*)(array + 2) = 
*((int16_t*)array + 1) = 
```

### 2.5. Xử lí chuỗi
#### a. Tính toán độ dài và kích thước (điền kết quả sau dấu =)
```c
char str[] = "hello";
strlen(str) = 
sizeof(str) = 
```
tương tự thay bằng
```c
char *str = "hello";
strlen(str) = 
sizeof(str) = 

char str[10] = "hello";
strlen(str) = 
sizeof(str) = 

char str[10] = {'h', 'e', '\0', 'l', 'l', 'o'};
strlen(str) = 
sizeof(str) = 
```

#### b. Viết chương trình tách chuỗi sau thành 3 chuỗi độc lập lưu vào các buffer KHÔNG sử dụng thư viện string.h
```c
char buffer[3][100];
char *str = "hello world !!!";
```
```















```

### 2.6. Nếu liên tục cấp phát động (malloc, calloc, realloc) nhưng không giải phóng (free) thì dẫn đến lỗi gì?
```
```
Nếu sử dụng các hàm đệ quy thì có thể dẫn đến lỗi gì?
```
```

### 2.7. Nêu 1 số điểm so sánh giữa mảng và danh sách liên kết (linked-list)
```
(ví dụ về sắp xếp trong bộ nhớ, khả năng thêm sửa xóa, truy xuất)







```

### 2.8. Tính giá trị biểu thức hậu tố sau (xem ví dụ để hiểu thêm)
```
5 1 2 + 4 * + 3 –
```
Kết quả
```
```
Ví dụ
```
7 2 + 3 *: áp dụng cơ chế stack ta có 
push(7) -> push(2) -> pop(2) và pop(7) thực hiện phép + -> push(9) -> push(3) -> pop(3) và pop(9) thực hiện phép * -> push(27)
Kết quả = 27
```

### 2.9. Kết quả cuối cùng của hàng đợi (Queue theo cơ chế FIFO: enqueue: đưa 1 phần tử vào hàng đợi; dequeue: lấy 1 phần tử ra khỏi hàng đợi)
```
enqueue(5), enqueue(3), dequeue(), enqueue(8), dequeue(), enqueue(2).
```
Kết quả
```
```
