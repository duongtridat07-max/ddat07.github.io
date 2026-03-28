
## 1. Công cụ AI sử dụng
* **Tên AI:** Gemini 3 Flash (Google)
* **Phiên bản:** Free Tier
* **Chế độ:** Code, reasoning and chat

## 2. Câu lệnh (Prompt) đã sử dụng
Để phát sinh mã CSS cho giao diện Apple chuẩn mẫu, tôi đã sử dụng chuỗi câu lệnh sau:

> **Prompt:** "Dựa trên file HTML tôi cung cấp, hãy viết mã CSS để tạo giao diện chuyên nghiệp giống hệt phong cách Apple. Yêu cầu: 
> 1. Sử dụng font chữ hệ thống -apple-system. 
> 2. Thanh navigation phải có hiệu ứng kính mờ (backdrop-filter: blur).
> 3. Nút bấm bo tròn dạng pill-shape.
> 4. Thêm hiệu ứng animation 'fadeInUp' cho tiêu đề và hình ảnh khi vừa tải trang để tăng tính thẩm mỹ."

## 3. Kết quả (Output - Mã nguồn CSS)

Dưới đây là đoạn mã CSS đã được AI tối ưu hóa để tạo giao diện Apple chuẩn mẫu:

```css
/* Reset căn bản & Font chữ hệ thống */
body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    background-color: #ffffff;
    color: #1d1d1f;
    -webkit-font-smoothing: antialiased;
    scroll-behavior: smooth;
}

/* 1. Thanh QuocGia (Thông báo) */
#QuocGia {
    background-color: #f5f5f7;
    padding: 12px 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 12px;
    gap: 15px;
    border-bottom: 1px solid #d2d2d7;
}

/* 2. Thanh Navigation (Hiệu ứng kính mờ) */
#navigation {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
    height: 44px;
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    position: sticky;
    top: 0;
    z-index: 99;
    border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

#navigation a {
    text-decoration: none;
    color: #424245;
    font-size: 12px;
    opacity: 0.8;
    transition: opacity 0.3s;
}

#navigation a:hover { opacity: 1; }

/* 3. Nội dung chính & Hiệu ứng */
#NoiDung {
    text-align: center;
    padding-top: 80px;
    background-color: #f5f5f7;
    min-height: 100vh;
}

#NoiDung h1 { font-size: 56px; font-weight: 600; margin-bottom: 0; }
#NoiDung h2 { font-size: 26px; font-weight: 400; margin-top: 10px; }

/* Nút bấm (Pill-shape) */
.cta-buttons { margin-top: 30px; }
button {
    padding: 12px 22px;
    border-radius: 980px;
    font-size: 17px;
    cursor: pointer;
    margin: 0 10px;
    border: none;
    transition: transform 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

button:active { transform: scale(0.95); } /* Hiệu ứng nhấn nút */

.btn-learn { background: #0071e3; color: white; }
.btn-buy { background: transparent; color: #0071e3; border: 1px solid #0071e3; }

/* Hiệu ứng xuất hiện (fadeInUp) */
@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

.product-info, .product-image {
    animation: fadeInUp 0.8s ease-out forwards;
}
