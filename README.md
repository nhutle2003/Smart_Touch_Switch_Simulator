Smart Touch Switch Simulator (STM32F401RE)
📌 Giới thiệu

Dự án xây dựng hệ thống mô phỏng công tắc cảm ứng cho nhà thông minh trên nền tảng vi điều khiển STM32F401RE (Nucleo).

Firmware được thiết kế theo kiến trúc hướng sự kiện (event-driven), kết hợp state machine và cấu trúc module hóa nhằm đảm bảo hệ thống hoạt động rõ ràng, dễ mở rộng và dễ bảo trì.

Hệ thống xử lý tương tác từ nút nhấn để điều khiển LED RGB, còi buzzer, hiển thị LCD và cập nhật dữ liệu cảm biến môi trường theo chu kỳ.

🔧 Chức năng chính

Hiển thị thông báo khởi động hệ thống trên LCD khi cấp nguồn.

Xử lý sự kiện nút nhấn:

Nhấn đơn: bật/tắt các màu LED RGB (Red, Green, Blue, White) kèm tín hiệu buzzer.

Nhấn 5 lần liên tiếp: hiển thị thông tin hệ thống.

Nhấn giữ: tăng/giảm độ sáng LED bằng điều khiển PWM.

Đọc và hiển thị dữ liệu cảm biến:

Nhiệt độ, độ ẩm qua giao tiếp I2C.

Cường độ ánh sáng qua ADC (DMA mode).

Cập nhật dữ liệu cảm biến định kỳ thông qua cơ chế timer scheduling.

🏗 Kiến trúc phần mềm

Thiết kế firmware theo mô hình hướng sự kiện (Event-driven).

Xây dựng state machine quản lý trạng thái hệ thống (Startup / Idle / Reset).

Sử dụng timer scheduler để thực thi các tác vụ định kỳ.

Tổ chức mã nguồn theo cấu trúc module (Core / Drivers).

🛠 Công nghệ sử dụng

Vi điều khiển: STM32F401RE

Ngôn ngữ lập trình: Embedded C

GPIO: xử lý nút nhấn

PWM: điều khiển độ sáng LED RGB

SPI: giao tiếp LCD

I2C: giao tiếp cảm biến nhiệt độ & độ ẩm

ADC + DMA: đọc cảm biến ánh sáng

📊 Luồng hoạt động hệ thống

Khởi tạo hệ thống và hiển thị thông báo khởi động.

Chuyển sang trạng thái chờ và xử lý sự kiện từ nút nhấn hoặc timer.

Điều khiển LED, buzzer và LCD tương ứng với sự kiện.

Định kỳ đọc và cập nhật dữ liệu cảm biến lên màn hình.
