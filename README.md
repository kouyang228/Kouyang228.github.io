<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的插畫作品集</title>
    <style>
        /* 1. 全域樣式與溫暖的背景色 */
        body {
            margin: 0;
            padding: 0;
            background-color: #fcf8f5; /* 帶有微細紋理感的暖白/米色調 */
            font-family: 'Noto Serif TC', 'Georgia', serif; /* 優雅的襯線體 */
            color: #4a4a4a;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* 2. 個人檔案區域（大頭貼與簡介） */
        .profile-container {
            text-align: center;
            padding: 60px 20px 30px 20px;
            max-width: 600px;
        }

        .avatar {
            width: 130px;
            height: 130px;
            border-radius: 50%; /* 完美圓形 */
            object-fit: cover;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            margin-bottom: 20px;
        }

        .name {
            font-size: 2.2rem;
            letter-spacing: 2px;
            color: #d47a83; /* 帶有設計感的粉色調 */
            margin: 10px 0 5px 0;
            font-weight: normal;
        }

        .title {
            font-size: 1rem;
            color: #a88d8f;
            margin-bottom: 15px;
            letter-spacing: 1px;
        }

        .bio {
            font-size: 0.95rem;
            line-height: 1.8;
            color: #706e6e;
            margin-top: 15px;
        }

        /* 3. 精緻的分隔線 */
        .divider {
            width: 100px;
            height: 1px;
            background-color: #e6dbd5;
            margin: 30px auto;
            position: relative;
        }
        .divider::after {
            content: '';
            position: absolute;
            top: -4px;
            left: 50%;
            transform: translateX(-50%);
            width: 9px;
            height: 9px;
            background-color: #fcf8f5;
            border: 1px solid #e6dbd5;
            border-radius: 50%; /* 小圓點裝飾 */
        }

        /* 4. 作品集網格區域（完美留白與正方形裁切） */
        .gallery-container {
            width: 100%;
            max-width: 1000px; /* 限制最大寬度，兩側留白 */
            padding: 0 24px 80px 24px; /* 確保手機版左右絕對不貼邊 */
            box-sizing: border-box;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* 電腦版一排3張 */
            gap: 20px; /* 圖片之間的間距 */
        }

        /* 手機與平版適應 */
        @media (max-width: 768px) {
            .gallery-grid {
                grid-template-columns: repeat(2, 1fr); /* 平板一排2張 */
                gap: 12px;
            }
            .profile-container { padding-top: 40px; }
        }
        @media (max-width: 480px) {
            .gallery-grid {
                grid-template-columns: repeat(1, 1fr); /* 手機版一排1張，直覺好看 */
                gap: 16px;
            }
        }

        /* 圖片容器：強制變成正方形 */
        .portfolio-item {
            position: relative;
            width: 100%;
            padding-top: 100%; /* 1:1 寬高比 */
            overflow: hidden;
            border-radius: 4px; /* 微乎其微的圓角，更有畫廊質感 */
            background-color: #eaeaea;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .portfolio-item:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.08);
        }

        .portfolio-item img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover; /* 核心：自動佔滿並裁切成正方形，不變形 */
        }

        /* 5. 點擊放大彈出視窗 (Lightbox) */
        .lightbox {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-color: rgba(252, 248, 245, 0.95);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        .lightbox img {
            max-width: 90%;
            max-height: 85%;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            border-radius: 4px;
        }
        .lightbox:target { display: flex; }
        .close-lightbox {
            position: absolute;
            top: 20px; right: 30px;
            font-size: 35px; color: #a88d8f;
            text-decoration: none;
        }
    </style>
</head>
<body>

    <!-- 個人檔案區 -->
    <div class="profile-container">
        <!-- 記得上傳一張叫 avatar.jpg 的大頭貼喔 -->
        <img src="avatar.jpg" alt="Avatar" class="avatar">
        
        <h1 class="name">你的名字</h1>
        <div class="title">Illustrator | 插畫家</div>
        
        <div class="bio">
            用畫筆紀錄日常碎片，分享色彩與故事。<br>
            歡迎來到我的個人作品集空間。
        </div>
    </div>

    <!-- 精緻小圓點分隔線 -->
    <div class="divider"></div>

    <!-- 作品集網格區 -->
    <div class="gallery-container">
        <div class="gallery-grid">
            
            <!-- 作品 1 -->
            <a href="#img1" class="portfolio-item">
                <img src="1.jpg" alt="作品 1">
            </a>
            <div id="img1" class="lightbox">
                <a href="#" class="close-lightbox">&times;</a>
                <img src="1.jpg" alt="作品 1 大圖">
            </div>

            <!-- 作品 2 -->
            <a href="#img2" class="portfolio-item">
                <img src="2.jpg" alt="作品 2">
            </a>
            <div id="img2" class="lightbox">
                <a href="#" class="close-lightbox">&times;</a>
                <img src="2.jpg" alt="作品 2 大圖">
            </div>

            <!-- 作品 3 -->
            <a href="#img3" class="portfolio-item">
                <img src="3.jpg" alt="作品 3">
            </a>
            <div id="img3" class="lightbox">
                <a href="#" class="close-lightbox">&times;</a>
                <img src="3.jpg" alt="作品 3 大圖">
            </div>

            <!-- 如果你有更多作品，可以把下面的註解拿掉，上傳 4.jpg, 5.jpg, 6.jpg -->
            <!--
            <a href="#img4" class="portfolio-item"><img src="4.jpg" alt="作品 4"></a>
            <div id="img4" class="lightbox"><a href="#" class="close-lightbox">&times;</a><img src="4.jpg"></div>

            <a href="#img5" class="portfolio-item"><img src="5.jpg" alt="作品 5"></a>
            <div id="img5" class="lightbox"><a href="#" class="close-lightbox">&times;</a><img src="5.jpg"></div>

            <a href="#img6" class="portfolio-item"><img src="6.jpg" alt="作品 6"></a>
            <div id="img6" class="lightbox"><a href="#" class="close-lightbox">&times;</a><img src="6.jpg"></div>
            -->

        </div>
    </div>

</body>
</html>
