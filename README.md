[README.md](https://github.com/user-attachments/files/27628649/README.md)
# F1 WebGL Showroom & Racing Simulator

Một showroom và trình giả lập đua xe Công thức 1 3D trên nền web được xây dựng bằng Three.js. Ứng dụng này cho phép người dùng khám phá một chiếc xe F1 chi tiết cao theo thông số kỹ thuật năm 2026, kiểm tra các bộ phận bên trong như động cơ V6 và pin ERS trong chế độ X-Ray, tùy chỉnh khí động học của xe và đưa xe ra đường đua để trải nghiệm giả lập đua xe chân thực đối đầu với các đối thủ AI.

## Các tính năng

### 🏁 Showroom & Garage F1
*   **Mô hình 3D chi tiết cao**: Xe F1 thông số 2026 với hệ thống đèn neon đầy đủ và môi trường garage mang phong cách Sci-Fi.
*   **Camera tương tác**: Kéo để xoay, cuộn để thu phóng, click chuột phải để di chuyển góc nhìn.
*   **Chế độ X-Ray & Phân lập bộ phận**: Lập tức tách riêng và quan sát các bộ phận bên trong như Động cơ Turbo V6, Pin ERS và Bộ tản nhiệt với các hiệu ứng chuyển đổi camera mượt mà của GSAP.
*   **Màu sơn đội đua**: Chọn từ 11 đội đua F1 chính thức (Ferrari, Mercedes, Red Bull, v.v.) và lập tức áp dụng màu sơn của họ lên mô hình xe.
*   **Kiểm tra tính hợp lệ theo luật FIA**: Điều chỉnh góc cánh trước/sau và sức mạnh động cơ. Hệ thống sẽ kiểm tra thiết lập của bạn dựa trên các quy định mô phỏng của FIA 2026 và đưa ra các cảnh báo ngay lập tức.

### 🏎️ Chế độ Đua xe
*   **Phiên phân hạng (Qualifying)**: Đưa xe F1 của bạn ra đường đua trong 3 vòng phân hạng để xác định vị trí xuất phát dựa trên thời gian vòng đua tốt nhất của bạn.
*   **Đối thủ AI**: Đua với 10 chiếc xe do AI điều khiển (đại diện cho các đội F1 khác) cùng chạy trên đường đua với bạn.
*   **Đội hình xuất phát xen kẽ**: Các xe được sắp xếp chính xác theo đội hình xuất phát xen kẽ truyền thống của F1 trên lưới xuất phát.
*   **Vật lý & Đo xa (Telemetry)**: Mô phỏng quá trình tăng tốc, phanh và đánh lái. Giao diện HUD đo xa theo thời gian thực hiển thị tốc độ KM/H, Số xe, Vòng tua máy (RPM), dung lượng pin ERS và tính khả dụng của DRS.
*   **Bản đồ thu nhỏ (Minimap)**: Bản đồ thu nhỏ của đường đua trực tiếp theo dõi vị trí chiếc xe của bạn và các đối thủ AI.
*   **Bấm giờ vòng đua & Kết quả**: Theo dõi chính xác thời gian hoàn thành vòng đua. Hiển thị kết quả Phân hạng tạm thời và kết quả Cuộc đua cuối cùng với khoảng cách thời gian so với người dẫn đầu.

## Điều khiển

*   **W / Mũi tên lên**: Tăng ga (Tăng tốc)
*   **S / Mũi tên xuống**: Phanh / Lùi xe
*   **A / Mũi tên trái**: Đánh lái sang trái
*   **D / Mũi tên phải**: Đánh lái sang phải
*   **Chuột**: Điều khiển camera trong Garage và quan sát cuộc đua trong Chế độ Đua xe.

## Cài đặt & Thiết lập

1.  **Clone repository:**
    ```bash
    git clone https://github.com/your-username/f1-showroom.git
    cd f1-showroom
    ```

2.  **Cài đặt các dependencies:**
    ```bash
    npm install
    ```

3.  **Chạy server phát triển (development server):**
    ```bash
    npm run dev
    ```

4.  **Mở trên trình duyệt:**
    Truy cập vào `http://localhost:5173` (hoặc URL do Vite cung cấp).

## Các công nghệ được sử dụng

*   **Three.js**: Lõi engine render 3D WebGL.
*   **GSAP**: Hiệu ứng hoạt hình và chuyển đổi camera hiệu suất cao.
*   **Vite**: Công cụ build frontend tốc độ cao.
*   **Vanilla JS / HTML / CSS**: Không sử dụng các UI framework nặng nề, tập trung hoàn toàn vào hiệu suất.

## Cấu trúc dự án

*   `src/main.js`: Điểm đầu vào chính (main entry point), thiết lập bối cảnh (scene), tải mô hình và vòng lặp render.
*   `src/race/raceMode.js`: Lõi logic đua xe, vật lý, dò đường đua (raycast track collision) và quản lý giai đoạn (Phân hạng/Đua).
*   `src/race/AIOpponents.js`: Tạo xe AI theo thủ tục, tính toán vị trí trên lưới xuất phát và AI đi theo lộ trình.
*   `src/race/result/ResultManager.js`: Các thuật toán xếp hạng và điều phối Giao diện Kết quả.
*   `src/ui/teamSelector.js`: Logic để thay đổi màu sắc đội đua và các mô hình.
*   `public/models/`: Chứa các mô hình GLTF/GLB cho đường đua, garage và các xe đội đua.

## Bản quyền

Dự án này được tạo ra cho mục đích giáo dục và xây dựng hồ sơ năng lực (portfolio). Formula 1 và tất cả các tên/logo của các đội đua có liên quan là nhãn hiệu của những chủ sở hữu tương ứng.
