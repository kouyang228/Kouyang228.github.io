<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的插畫作品集 | My Portfolio</title>
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }

        header {
            text-align: center;
            padding: 60px 20px;
            background-color: #fff;
            border-bottom: 1px solid #eee;
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
            letter-spacing: 2px;
        }

        header p {
            margin: 10px 0 0 0;
            color: #888;
            font-size: 1.1rem;
        }

        .portfolio-container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }

        .artwork-card {
            background-color: #fff;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
        }

        .artwork-card:hover {
            transform: translateY(-5px);
        }

        .artwork-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            display: block;
        }

        .artwork-info {
            padding: 15px;
        }

        .artwork-info h3 {
            margin: 0 0 8px 0;
            font-size: 1.2rem;
        }

        .artwork-info p {
            margin: 0;
            color: #666;
            font-size: 0.9rem;
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            color: #aaa;
            font-size: 0.85rem;
        }
    </style>
</head>
<body>

    <!-- 頁首區塊：可以改成你的名字 -->
    <header>
        <h1>我的插畫作品集</h1>
        <p>歡迎來到我的創作空間</p>
    </header>

    <!-- 作品展示區塊 -->
    <div class="portfolio-container">
        <div class="gallery">
            
            <!-- 第一張作品 -->
            <div class="artwork-card">
                <img src="1.JPG" alt="作品一">
                <div class="artwork-info">
                    <h3>作品一標題</h3>
                    <p>在這裡輸入這幅畫的說明或年份</p>
                </div>
            </div>

            <!-- 第二張作品 -->
            <div class="artwork-card">
                <img src="2.JPG" alt="作品二">
                <div class="artwork-info">
                    <h3>作品二標題</h3>
                    <p>在這裡輸入這幅畫的說明或年份</p>
                </div>
            </div>

            <!-- 第三張作品 -->
            <div class="artwork-card">
                <img src="3.JPG" alt="作品三">
                <div class="artwork-info">
                    <h3>作品三標題</h3>
                    <p>在這裡輸入這幅畫的說明或年份</p>
                </div>
            </div>

        </div>
    </div>

    <!-- 頁尾 -->
    <footer>
        <p>&copy; 2026 你的名字. All Rights Reserved.</p>
    </footer>

</body>
</html>

