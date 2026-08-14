# Mạch phát âm thanh MKE-M11 JQ8900 MP3 I2C Module

## Giới thiệu
Mạch phát âm thanh MKE-M11 JQ8900 MP3 I2C Module là mạch phát âm thanh sử dụng module JQ8900, cho phép phát các file âm thanh định dạng **MP3/WAV** được lưu trữ trên bộ nhớ Flash tích hợp. Module có thể kết nối trực tiếp với máy tính thông qua cổng **Micro USB** và được nhận dạng như một thiết bị lưu trữ USB, giúp người dùng dễ dàng chép và cập nhật các file âm thanh. Module tích hợp bộ nhớ Flash dung lượng **4MB (32Mbit)**, phù hợp để lưu trữ các file âm thanh như nhạc nền, hiệu ứng âm thanh, lời thoại, thông báo và các đoạn âm thanh hướng dẫn.

Mạch phát âm thanh MKE-M11 JQ8900 MP3 I2C Module được tích hợp MCU giúp chuyển đổi và xử lý giao tiếp theo chuẩn **I2C**, cho phép vi điều khiển điều khiển module chỉ với hai dây tín hiệu **SDA** và **SCL**. Địa chỉ I2C mặc định là **50 (0x32)** và có thể cấu hình nhiều địa chỉ khác nhau. Module tích hợp sẵn **loa mini 3W 8Ω** có vỏ bảo vệ, cho phép phát âm thanh trực tiếp mà không cần sử dụng thêm mạch khuếch đại trong các ứng dụng cơ bản.

Sản phẩm có thể được sử dụng trong nhiều ứng dụng thực tế như:
- Phát lời thoại hướng dẫn cho robot.
- Phát âm thanh cảnh báo.
- Phát nhạc nền cho mô hình robot.
- Phát hiệu ứng âm thanh cho các dự án STEM.
- Phát thông báo trạng thái của thiết bị.
- Xây dựng các hệ thống hướng dẫn bằng giọng nói.
- Robot tương tác bằng âm thanh.
- Mô hình nhà thông minh.
- Các dự án IoT có phản hồi bằng âm thanh.

Mạch phát âm thanh MKE-M11 JQ8900 MP3 I2C Module đặc biệt phù hợp cho các **mô hình robot, dự án STEM, đồ án học tập và thực hành điện – điện tử**, giúp người học dễ dàng tiếp cận cách lưu trữ dữ liệu âm thanh, điều khiển thiết bị ngoại vi bằng giao tiếp I2C và xây dựng các hệ thống tương tác bằng âm thanh. Module hỗ trợ điện áp giao tiếp **3.3VDC và 5VDC**, cho phép kết nối với Arduino, Raspberry Pi, NVIDIA Jetson, Micro:bit và nhiều nền tảng điều khiển khác. Module sử dụng chuẩn kết nối **XH2.54 4P** và đi kèm cáp **4P XH2.54 – Dupont**.

## Thông số kỹ thuật
- Module chính: JQ8900
- Điện áp hoạt động: 5VDC
- Bộ nhớ Flash: 4MB (32Mbit)
- Định dạng âm thanh:
  - MP3
  - WAV
- Chuẩn giao tiếp: I2C
- Địa chỉ I2C mặc định: `50 (0x32)`
- Địa chỉ I2C có thể cấu hình: `50 – 55`
- Điện áp giao tiếp: TTL 3.3VDC / 5VDC
- Loa tích hợp:
  - Công suất: 3W
  - Trở kháng: 8Ω
  - Loại: Loa đơn mini có vỏ bảo vệ
- Kết nối máy tính:
  - Micro USB
  - Nhận dạng như USB Flash
  - Cho phép chép file âm thanh trực tiếp vào bộ nhớ Flash
- Chức năng điều khiển:
  - Play
  - Pause
  - Stop
  - Next
  - Previous
  - Điều chỉnh âm lượng
  - Phát file theo số thứ tự
  - Phát file trong thư mục
  - Chèn file âm thanh trong khi đang phát
- Khả năng tương thích:
  - Arduino
  - Raspberry Pi
  - NVIDIA Jetson
  - Micro:bit
  - Và các board điều khiển 3.3VDC / 5VDC khác
- Thiết kế mạch:
  - Hoạt động ổn định
  - Giao tiếp I2C đơn giản
  - Tích hợp bộ nhớ Flash
  - Tích hợp loa
  - Phù hợp cho ứng dụng học tập và thực tế
- Chuẩn kết nối: XH2.54 4P
- Đi kèm cáp kết nối: 4P XH2.54 – Dupont

## Các chân tín hiệu

| Chân | Chức năng |
|------|-----------|
| GND | Nguồn âm 0VDC |
| 5V | Nguồn dương 5VDC |
| SDA | Chân I2C Data |
| SCL | Chân I2C Clock |

## Hướng dẫn cấu hình

### Kết nối máy tính và chép file MP3/WAV
Kết nối MKE-M11 với máy tính thông qua cổng **Micro USB**. Máy tính sẽ nhận bộ nhớ Flash 4MB của module như một thiết bị lưu trữ USB. Sau khi kết nối, người dùng có thể chép các file MP3/WAV vào bộ nhớ Flash.
> **Lưu ý:** Thư mục `MF` là thư mục hệ thống dành riêng cho module. **Không được xóa hoặc chỉnh sửa các file bên trong thư mục này.**
Khi chép file âm thanh mới, chỉ sử dụng:
- Thư mục gốc `Root`.
- Các thư mục số từ `01` đến `99`.

### Quy tắc đặt tên file
| Vị trí | Quy tắc | Ví dụ |
|--------|---------|-------|
| Root | 5 ký tự đầu tiên bắt buộc là số | `00001_BackgroundMusic.mp3` |
| Folder `01–99` | 3 ký tự đầu tiên bắt buộc là số | `001_BaiHat1.mp3` |
| Folder `MF` | 3 ký tự đầu tiên bắt buộc là số | `002_Enter_SetupAddress.mp3` |

### Cấu trúc thư mục
```text
Flash JQ8900 (4MB)
│
├── MF/                         # HỆ THỐNG - KHÔNG XÓA / KHÔNG SỬA
│   ├── 001_Reset completed.mp3
│   ├── 002_Enter_SetupAddress.mp3
│   ├── 003_AddressSaved.mp3
│   └── ...
│
├── 01/                         # Thư mục người dùng
│   ├── 001_BaiHat1.mp3
│   ├── 002_BaiHat2.mp3
│   └── ...
│
├── 02/
│   ├── 001_QuangCao.mp3        # Thư mục người dùng
│   └── 002_ThongBao.mp3
│
├── 03/
│   └── 001_EffectSound.mp3     # Thư mục người dùng
│
├── ...
│
├── 00001_BackgroundMusic.mp3   # Thư mục gốc Root
├── 00002_Song.mp3
└── 00003_Welcome.mp3
```
![MKE-M11 I2C_JQ8900 MP3](/extras/MKE-M11_0.png)

## Cấu hình địa chỉ I2C
MKE-M11 tích hợp một nút nhấn cho phép kiểm tra và thay đổi địa chỉ I2C mà không cần viết chương trình.

### Xem địa chỉ I2C hiện tại
- Nhấn nút **1 lần (Click)**.
- Module sẽ phát thông báo về địa chỉ I2C hiện tại, ví dụ: "Địa chỉ hiện tại là: Năm Không" nếu đang ở địa chỉ mặc định 50 (0x32).

### Thay đổi địa chỉ I2C

- Nhấn và giữ nút khoảng **3 giây**.
- Khi module phát thông báo: "Đang vào chế độ cài đặt địa chỉ"
- Thả nút ra.
- Nhấn nút **2 lần liên tiếp nhanh (Double-click)** để đổi địa chỉ mới, mỗi lần Double-click, địa chỉ I2C tăng lên 1 (từ 50 lên tối đa 55, sau đó quay vòng về 50).
- Nhấn và giữ nút khoảng **3 giây** để lưu địa chỉ đã cài đặt, module phát thông báo: "Đã lưu địa chỉ!" là hoàn tất.
> **Lưu ý:** Trong quá trình cài đặt, nếu nhấn nút **1 lần** mạch sẽ báo "đã hủy bỏ", giữ lại cấu hình trước đó và thoát chế độ cài đặt.

### Khôi phục cài đặt gốc
- Nhấn và giữ nút khoảng **6 giây liên tục**.
- Module sẽ phát thông báo: "Khôi phục cài đặt gốc hoàn tất", địa chỉ I2C được đưa về mặc định là 50 (0x32).

## Giao thức I2C cấp thấp

MKE-M11 giao tiếp với vi điều khiển chính (Master) thông qua giao thức I2C. Địa chỉ mặc định: 50 (0x32)

### Cấu trúc gói tin

```text
[AddressId] [ModeId] [Value32]
```

| Thành phần | Kích thước | Mô tả |
|------------|------------|-------|
| `AddressId` | 1 byte | Địa chỉ module |
| `ModeId` | 1 byte | Mã lệnh |
| `Value32` | 4 bytes | Giá trị truyền hoặc nhận |

### Lệnh hệ thống

| Mode ID | Tên lệnh | Chức năng | Value |
|---------|----------|-----------|-------|
| `1` | `SetAddress` | Đổi địa chỉ I2C | Địa chỉ mới `0–127` |
| `10` | `GetAddress` | Đọc địa chỉ I2C hiện tại | Địa chỉ đang sử dụng |
| `10` | `GetAddress` | Đọc địa chỉ I2C hiện tại | Địa chỉ đang sử dụng |
| `200` | `Set_Admin_Mode` | Mở/khóa quyền Admin | `0xA5A5A5A5` |

### Lệnh điều khiển MP3

| Mode ID | Tên lệnh | Chức năng | Value |
|---------|----------|-----------|-------|
| `50` | `MP3_Play` | Tiếp tục phát | `0` |
| `51` | `MP3_Pause` | Tạm dừng | `0` |
| `52` | `MP3_Stop` | Dừng phát | `0` |
| `53` | `MP3_Next` | Bài tiếp theo | `0` |
| `54` | `MP3_Prev` | Bài trước | `0` |
| `55` | `MP3_Set_Volume` | Chỉnh âm lượng | `0–30` |
| `56` | `MP3_Play_Track` | Phát bài theo số thứ tự trong Root | Số file |
| `57` | `MP3_Get_Status` | Đọc trạng thái phát | `1=Play`, `2=Pause`, `0=Stop` |
| `58` | `MP3_Get_Volume` | Đọc âm lượng hiện tại | `0–30` |
| `59` | `MP3_Play_Track_in_Folder_Number` | Phát file trong thư mục số | `Folder × 1000 + File` |
| `60` | `MP3_Play_Track_in_Folder_MF` | Phát file trong thư mục `MF` | Số file |
| `61` | `MP3_Play_Insert_Track` | Chèn file âm thanh khi đang phát | Số file |
| `62` | `MP3_Play_Insert_Track_in_Folder_Number` | Chèn file từ thư mục số | `Folder × 1000 + File` |
| `63` | `MP3_Play_Insert_Track_in_Folder_MF` | Chèn file từ thư mục `MF` | Số file |

### Chương trình mô tả giao tiếp I2C cấp thấp trên Arduino

Ví dụ dưới đây phát file số `00001` trong thư mục Root và đọc âm lượng hiện tại của module.

```cpp
#include <Wire.h>
#include <MKE_I2C_MP3.h>

MKE_I2C_MP3 mp3;

#define MP3_I2C_ADDRESS 50 // 0x32 - Địa chỉ mặc định

void setup() {
  Serial.begin(115200);

  // Khởi tạo module MP3
  mp3.begin(MP3_I2C_ADDRESS);
  delay(1000);

  // Thiết lập âm lượng
  Serial.println("Set volume 20");
  if (mp3.setVolume(20) == 0) {
    Serial.println("Set volume OK");
  } else {
    Serial.println("Set volume ERROR");
  }

}

void loop() {
  uint8_t volume;
  MKE_I2C_MP3::Status status;
  // Phát file số 00001 trong thư mục Root
  if (mp3.playTrack(1) == 0) {
    Serial.println("Playing track 2...");
  } else {
    Serial.println("Play track ERROR");
  }
  delay(1000);

  // Đọc trạng thái phát
  Serial.print("Status: ");
  Serial.println(mp3.getStatus(status));

  // Đọc âm lượng hiện tại
  Serial.print("Volume: ");
  Serial.println(mp3.getVolume(volume));

  // Chờ 5 giây
  delay(5000);

  // Tạm dừng
  mp3.pause();
  Serial.println("Pause");

  // Chờ 2 giây
  delay(2000);

  // Tiếp tục phát
  mp3.play();
  Serial.println("Play");
}
```
## Bộ thư viện MKE_I2C_MP3

Thư viện `MKE_I2C_MP3` cung cấp các hàm điều khiển MKE-M11 JQ8900 thông qua giao tiếp I2C, giúp đơn giản hóa việc lập trình và không cần trực tiếp xử lý giao thức I2C cấp thấp.

### Khởi tạo thư viện
Tạo đối tượng `MKE_I2C_MP3`:
```cpp
#include <MKE_I2C_MP3.h>
MKE_I2C_MP3 mp3;
```
MKE_I2C_MP3 không nhận tham số trong constructor. Mọi thiết lập ban đầu được đưa vào begin().

### Khởi tạo với Bus I2C mặc định
Địa chỉ I2C mặc định của MKE-M11 là `50 (0x32)`, Bus I2C mặc định là `Wire`.
```cpp
mp3.begin(50);
```

### Sử dụng bus I2C khác
Đối với các MCU hỗ trợ nhiều bus I2C, có thể chỉ định bus I2C cần sử dụng:
```cpp
mp3.begin(50, Wire2);
```
Trong đó:
- `50`: Địa chỉ I2C mặc định của module.
- `Wire2`: Bus I2C Wire2 được sử dụng.

### Thay đổi địa chỉ I2C bằng thư viện

Để thay đổi địa chỉ I2C bằng phần mềm, cần mở **Admin Mode** trước khi thực hiện thay đổi. Ví dụ chuyển địa chỉ từ `50` sang `51`:

```cpp
mp3.setAdminMode(true);

delay(10);

mp3.changeModuleAddress(51);

mp3.setAdminMode(false);
```
> **Lưu ý:** Luôn mở Admin Mode trước khi gọi `changeModuleAddress()`.


### Các hàm điều khiển và phát nhạc

Các hàm điều khiển phát nhạc trả về mã `Wire.endTransmission()`:
  - `0`: Gửi lệnh thành công.
  - Khác `0`: Có lỗi giao tiếp I2C.

Các hàm đọc như `getVolume()`, `getStatus()`, `getModuleId()` và `readModuleAddress()`
  - Trả về `true` khi nhận đủ 4 bytes dữ liệu.
  - Trả về `false` khi giao tiếp thất bại.

| Hàm | Tham số / Giá trị | Mô tả |
|------|-------------------|-------|
| `mp3.play()` | `-` | Tiếp tục phát file âm thanh hiện tại |
| `mp3.pause()` | `-` | Tạm dừng phát |
| `mp3.stop()` | `-` | Dừng phát |
| `mp3.next()` | `-` | Chuyển sang file tiếp theo |
| `mp3.previous()` | `-` | Chuyển về file trước |
| `mp3.setVolume()` | `0–30` | Thiết lập âm lượng |
| `mp3.playTrack()` | `track` | Phát file theo số thứ tự trong thư mục Root |
| `mp3.playTrackInFolder()` | `folder, track` | Phát file theo số thứ tự trong thư mục `01–99` |
| `mp3.playTrackInMF()` | `track` | Phát file trong thư mục hệ thống `MF` |
| `mp3.playInsertTrack()` | `track` | Chèn file âm thanh trong Root khi đang phát |
| `mp3.playInsertTrackInFolder()` | `folder, track` | Chèn file trong thư mục `01–99` khi đang phát |
| `mp3.playInsertTrackInMF()` | `track` | Chèn file trong thư mục `MF` khi đang phát |
| `mp3.getVolume()` | `volume` | Đọc âm lượng hiện tại |
| `mp3.getStatus()` | `status` | Đọc trạng thái phát nhạc |
| `mp3.getModuleId()` | `moduleId` | Đọc mã định danh module |
| `mp3.readModuleAddress()` | `address` | Đọc địa chỉ I2C hiện tại |
| `mp3.setAdminMode()` | `true / false` | Mở hoặc đóng Admin Mode |
| `mp3.changeModuleAddress()` | `address` | Thay đổi địa chỉ I2C của module |

| Hàm | Ví dụ | Ý nghĩa |
|------|-------|---------|
| `setVolume(volume)` | `setVolume(20)` | Đặt âm lượng ở mức `20` |
| `playTrack(track)` | `playTrack(2)` | Phát file `00002_*.mp3` trong Root |
| `playTrackInFolder(folder, track)` | `playTrackInFolder(2, 5)` | Phát file `005_*.mp3` trong thư mục `02` |
| `playTrackInMF(track)` | `playTrackInMF(1)` | Phát file số `1` trong thư mục `MF` |
| `playInsertTrack(track)` | `playInsertTrack(3)` | Chèn file số `3` trong Root |
| `playInsertTrackInFolder(folder, track)` | `playInsertTrackInFolder(2, 5)` | Chèn file số `5` trong thư mục `02` |
| `playInsertTrackInMF(track)` | `playInsertTrackInMF(1)` | Chèn file số `1` trong thư mục `MF` |

### Code mẫu sử dụng thư viện MKE_I2C_MP3

Ví dụ dưới đây sử dụng Arduino Uno hoặc ESP32 để:

1. Khởi tạo module tại địa chỉ I2C `50`.
2. Thiết lập âm lượng `20`.
3. Phát file số `00001` trong thư mục Root.
4. Đọc trạng thái phát nhạc.
5. Đọc âm lượng hiện tại.
6. Tạm dừng phát.
7. Tiếp tục phát.

```cpp
#include <Wire.h>
#include <MKE_I2C_MP3.h>

MKE_I2C_MP3 mp3;

#define MP3_I2C_ADDRESS 50 // 0x32 - Địa chỉ mặc định

void setup() {
  Serial.begin(115200);

  // Khởi tạo module MP3
  mp3.begin(MP3_I2C_ADDRESS);
  delay(1000);

  // Thiết lập âm lượng
  Serial.println("Set volume 20");
  if (mp3.setVolume(20) == 0) {
    Serial.println("Set volume OK");
  } else {
    Serial.println("Set volume ERROR");
  }

}

void loop() {
  uint8_t volume;
  MKE_I2C_MP3::Status status;
  // Phát file số 00001 trong thư mục Root
  if (mp3.playTrack(1) == 0) {
    Serial.println("Playing track 2...");
  } else {
    Serial.println("Play track ERROR");
  }
  delay(1000);

  // Đọc trạng thái phát
  Serial.print("Status: ");
  Serial.println(mp3.getStatus(status));

  // Đọc âm lượng hiện tại
  Serial.print("Volume: ");
  Serial.println(mp3.getVolume(volume));

  // Chờ 5 giây
  delay(5000);

  // Tạm dừng
  mp3.pause();
  Serial.println("Pause");

  // Chờ 2 giây
  delay(2000);

  // Tiếp tục phát
  mp3.play();
  Serial.println("Play");
}
```

### Lưu ý khi sử dụng thư viện
- Địa chỉ I2C mặc định của MKE-M11 là `50 (0x32)`.
- Gọi `mp3.begin()` một lần trong `setup()`.
- Kiểm tra nguồn cấp, dây `SDA`, `SCL`, `GND` và địa chỉ I2C nếu giao tiếp thất bại.
- Khi sử dụng `changeModuleAddress()`, cần mở Admin Mode trước.
- Không xóa hoặc chỉnh sửa thư mục `MF` trong bộ nhớ Flash.

## Hướng dẫn sử dụng

### Hướng dẫn kết nối
- Cấp nguồn 5VDC cho mạch qua hai chân GND và 5V.
- Kết nối chân SCL của Sensor với chân I2C Clock của mạch điều khiển.
- Kết nối chân SDA của Sensor với chân I2C Data của mạch điều khiển.

### Hướng dẫn sử dụng với Arduino Uno / Vietduino Uno / ESP32
- Trong **Tools / Library Manager**, tìm và cài đặt bộ thư viện tổng hợp **"MKE_ONE" by MakerEdu.vn**
- Mở chương trình mẫu tại **File / Examples / MKE_ONE / Module / MKE_M11_I2C_JQ8900_MP3**
- Cấu hình board mạch tương ứng là **Arduino Uno / ESP32**, chọn đúng cổng **COM Port** của mạch và nhấn **Upload** để nạp chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân SDA và SCL của Module với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

### Hướng dẫn lập trình với Micro:bit (kéo thả khối)

- Khởi động [Microsoft MakeCode](https://makecode.microbit.org/) và **Import** chương trình theo đường link sau: `https://github.com/makereduvn/mke_m11_i2c_jq8900_mp3_microbit/`
- Kết nối mạch Micro:bit và **Download** chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân SDA và SCL của Module với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

Nếu bắt đầu tự án mới cần cài đặt Extension **MKE_ONE_MICROBIT** trên [Microsoft MakeCode](https://makecode.microbit.org/) theo [hướng dẫn tại đây](https://github.com/makereduvn/MKE_ONE_MICROBIT). Sau khi cài đặt thành công, các khối lệnh của Extension **MKE_ONE_MICROBIT** sẽ xuất hiện trong danh sách block và sẵn sàng để sử dụng.

## Kích thước sản phẩm
![MKE-M11 I2C_JQ8900 MP3](/extras/MKE-M11_1.jpg)

## Hình ảnh sản phẩm
![MKE-M11 I2C_JQ8900 MP3](/extras/MKE-M11_2.jpg)
![MKE-M11 I2C_JQ8900 MP3](/extras/MKE-M11_3.jpg)
![MKE-M11 I2C_JQ8900 MP3](/extras/MKE-M11_4.jpg)

## Miễn trừ trách nhiệm
Sản phẩm này là bo mạch phát triển được thiết kế phục vụ cho mục đích nghiên cứu, thử nghiệm và học tập, không phải là một thiết bị hoàn chỉnh. Trong trường hợp người dùng kết hợp mạch này với các linh kiện, thiết bị hoặc phần mềm khác để tạo thành một hệ thống hoặc sản phẩm hoàn chỉnh, mọi chức năng và tính phù hợp của sản phẩm sau cùng đều thuộc trách nhiệm của người dùng.
