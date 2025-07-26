<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cửa hàng Mini App</title>

    <!-- Phần CSS (Styling) -->
    <style>
        :root {
            /* Sử dụng các biến màu của Telegram để giao diện đồng bộ */
            --tg-theme-bg-color: var(--tg-color-scheme, light) == 'light' ? #ffffff : #212121;
            --tg-theme-text-color: var(--tg-color-scheme, light) == 'light' ? #000000 : #ffffff;
            --tg-theme-hint-color: #999999;
            --tg-theme-link-color: #2481cc;
            --tg-theme-button-color: #2481cc;
            --tg-theme-button-text-color: #ffffff;
            --tg-theme-secondary-bg-color: var(--tg-color-scheme, light) == 'light' ? #f1f1f1 : #3a3a3a;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--tg-theme-bg-color);
            color: var(--tg-theme-text-color);
            margin: 0;
            padding: 15px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            box-sizing: border-box;
        }

        .container {
            text-align: center;
            width: 100%;
            max-width: 400px;
        }

        .product {
            background-color: var(--tg-theme-secondary-bg-color);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .product img {
            max-width: 120px;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .product h2 {
            margin: 0 0 10px 0;
            font-size: 1.2em;
        }

        .description {
            font-size: 0.9em;
            color: var(--tg-theme-hint-color);
            margin-bottom: 20px;
        }

        /* Phần chọn số lượng */
        .quantity-selector {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 20px;
        }

        .quantity-selector button {
            width: 40px;
            height: 40px;
            font-size: 1.5em;
            border: 1px solid var(--tg-theme-hint-color);
            background-color: transparent;
            color: var(--tg-theme-text-color);
            border-radius: 8px;
            cursor: pointer;
        }

        .quantity-selector input {
            width: 50px;
            height: 40px;
            text-align: center;
            font-size: 1.2em;
            border: 1px solid var(--tg-theme-hint-color);
            border-radius: 8px;
            margin: 0 10px;
            background-color: var(--tg-theme-bg-color);
            color: var(--tg-theme-text-color);
            -moz-appearance: textfield; /* Tắt mũi tên tăng/giảm trên Firefox */
        }
        
        .quantity-selector input::-webkit-outer-spin-button,
        .quantity-selector input::-webkit-inner-spin-button {
             -webkit-appearance: none; /* Tắt mũi tên tăng/giảm trên Chrome, Safari */
             margin: 0;
        }

        .price {
            font-size: 1.4em;
            font-weight: bold;
            color: var(--tg-theme-link-color);
            margin: 20px 0;
        }

        #buyButton {
            background-color: var(--tg-theme-button-color);
            color: var(--tg-theme-button-text-color);
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            font-size: 1.1em;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: background-color 0.2s ease;
        }
        
        #buyButton:hover {
            opacity: 0.9;
        }

        #userInfo {
            margin-top: 20px;
            font-size: 0.9em;
            color: var(--tg-theme-hint-color);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="product">
            <img src="https://i.imgur.com/k2yYmO8.png" alt="Ebook Cover">
            <h2>Ebook: Lập trình Bot Telegram</h2>
            <p class="description">Cuốn sách toàn diện giúp bạn bắt đầu xây dựng bot Telegram của riêng mình.</p>
            
            <!-- Bộ chọn số lượng -->
            <div class="quantity-selector">
                <button id="minusButton">-</button>
                <input type="number" id="quantityInput" value="1" min="1">
                <button id="plusButton">+</button>
            </div>

            <!-- Giá tiền (sẽ được cập nhật bằng JS) -->
            <p class="price" id="priceDisplay">Giá: 10 Stars ✨</p>
            
            <button id="buyButton">Thanh toán</button>
        </div>
        <div id="userInfo"></div>
    </div>

    <!-- Script kết nối với Telegram Web App API -->
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    
    <!-- Phần JavaScript (Logic) -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Khởi tạo đối tượng Telegram Web App
            const tg = window.Telegram.WebApp;
            
            // Cấu hình cơ bản cho Mini App
            tg.ready();
            tg.expand();

            // Thông tin sản phẩm
            const productId = 'ebook_telegram_dev_01';
            const basePrice = 10; // Giá cho 1 sản phẩm

            // Lấy các phần tử từ HTML
            const user = tg.initDataUnsafe?.user;
            const buyButton = document.getElementById('buyButton');
            const userInfoDiv = document.getElementById('userInfo');
            const quantityInput = document.getElementById('quantityInput');
            const minusButton = document.getElementById('minusButton');
            const plusButton = document.getElementById('plusButton');
            const priceDisplay = document.getElementById('priceDisplay');

            // Hàm cập nhật giá tiền trên giao diện
            const updatePrice = () => {
                const quantity = parseInt(quantityInput.value);
                const totalPrice = quantity * basePrice;
                priceDisplay.innerText = `Giá: ${totalPrice} Stars ✨`;
            };

            // Gán sự kiện cho các nút tăng/giảm số lượng
            plusButton.addEventListener('click', () => {
                quantityInput.value = parseInt(quantityInput.value) + 1;
                updatePrice();
            });

            minusButton.addEventListener('click', () => {
                let currentQuantity = parseInt(quantityInput.value);
                if (currentQuantity > 1) {
                    quantityInput.value = currentQuantity - 1;
                    updatePrice();
                }
            });

            // Gán sự kiện khi người dùng tự nhập số lượng
            quantityInput.addEventListener('change', () => {
                if (parseInt(quantityInput.value) < 1 || !quantityInput.value) {
                    quantityInput.value = 1;
                }
                updatePrice();
            });

            // Hiển thị lời chào nếu có thông tin người dùng
            if (user) {
                userInfoDiv.innerHTML = `Xin chào, <strong>${user.first_name || 'bạn'}</strong>!`;
            } else {
                userInfoDiv.innerHTML = 'Mở trong Telegram để thanh toán.';
                buyButton.disabled = true; // Vô hiệu hóa nút mua nếu không mở trong Telegram
            }

            // Xử lý sự kiện khi người dùng nhấn nút "Thanh toán"
            buyButton.addEventListener('click', () => {
                const currentQuantity = parseInt(quantityInput.value);
                const totalPrice = currentQuantity * basePrice;
                
                // ---- LƯU Ý QUAN TRỌNG ----
                // Đây là phần bạn phải tương tác với backend của mình.
                // 1. Gửi yêu cầu tới server của bạn với thông tin (productId, currentQuantity, totalPrice).
                // 2. Server của bạn gọi API của Telegram để tạo hóa đơn (createInvoiceLink) với giá tiền tương ứng.
                // 3. Server của bạn trả về một "invoice_slug" hoặc "payload" duy nhất.
                // 4. Bạn sử dụng payload đó để gọi hàm openInvoice.
                
                // GIẢ LẬP: Giả sử backend trả về một slug hóa đơn
                const invoiceSlug = `invoice_${productId}_qty${currentQuantity}_${new Date().getTime()}`;
                
                tg.openInvoice(invoiceSlug, (status) => {
                    // Callback này được gọi sau khi thanh toán hoàn tất (hoặc bị hủy)
                    if (status === 'paid') {
                        // Thanh toán thành công, có thể hiển thị thông báo cảm ơn
                        tg.showAlert('Cảm ơn bạn đã mua hàng!');
                        tg.close(); // Đóng Mini App
                    } else if (status === 'failed') {
                        // Thanh toán thất bại
                        tg.showAlert('Thanh toán không thành công. Vui lòng thử lại.');
                    } else if (status === 'cancelled') {
                        // Người dùng hủy
                        tg.showAlert('Giao dịch đã được hủy.');
                    }
                });
            });
            
            // Cập nhật giá ban đầu
            updatePrice();
        });
    </script>
</body>
</html>
