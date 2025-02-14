<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GALAXY STORE</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-image: url('https://arabradio.us/wp-content/uploads/2019/12/%D8%B5%D9%88%D8%B1-%D8%A7%D9%84%D9%81%D8%B6%D8%A7%D8%A1-16.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            transition: background-image 0.5s ease;
            padding: 20px;
        }
        .content {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            width: 90%;
            max-width: 500px;
            transition: all 0.5s ease;
            text-align: center;
        }
        input, button {
            padding: 14px;
            margin: 10px 0;
            font-size: 16px;
            width: 100%;
            box-sizing: border-box;
        }
        button {
            cursor: pointer;
            background-color: rgba(255, 255, 255, 0.2);
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: rgba(255, 255, 0.4);
        }
        #result {
            font-size: 18px;
            margin-top: 20px;
        }
        .product-list {
            margin-top: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        .product-card {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
        }
        footer {
            margin-top: auto;
            padding: 10px;
            font-size: 14px;
            opacity: 0.8;
        }
        @media (max-width: 768px) {
            .content {
                width: 100%;
            }
        }
        @media (max-width: 480px) {
            input, button {
                font-size: 14px;
                padding: 10px;
            }
            #result {
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <title>talal_megumi</title>
    <div class="content">
        <h1>GALAXY STORE</h1>
        <p>مرحبًا بكم في متجر المجرة! إليكم المنتجات المتاحة:</p>
        <div class="product-list" id="productList"></div>
    </div>
    
    <footer>
        <p>حقوق الطبع والنشر © <a href="https://www.instagram.com/talal_megumi" target="_blank">talal_megumi</a></p>
    </footer>

    <script>
        const products = [
            { name: "تغير لقب يوم", price: "50 ستارز" },
            { name: "تغير لقب ثلاث ايام", price: "150 ستارز" },
            { name: "تغير لقب اسبوع", price: "300 ستارز" },
            { name: "حذف انذار", price: "150 ستارز" },
            { name: "حذف انذارين", price: "250 ستارز" },
            { name: "تغير صورة كوكب يوم", price: "50 ستارز" },
            { name: "تغير صورة كوكب ثلاث ايام", price: "150 ستارز" },
            { name: "تغير اسم الكوكب يوم", price: "50 ستارز" },
            { name: "تغير اسم الكوكب ثلاث ايام", price: "100 ستارز" },
            { name: "زيارة يوم", price: "50 ستارز" },
            { name: "زيارة يومين", price: "100 ستارز" },
            { name: "زيارة ثلاثة ايام", price: "150 ستارز" }
        ];

        // Display products immediately when the page loads
        function displayProducts() {
            const productListDiv = document.getElementById("productList");
            productListDiv.innerHTML = products.map(product => `
                <div class="product-card">
                    <h3>${product.name}</h3>
                    <p>السعر: ${product.price}</p>
                </div>
            `).join('');
        }

        // Call function to display products on page load
        displayProducts();
    </script>
</body>
</html>
