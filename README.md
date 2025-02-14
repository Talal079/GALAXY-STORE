
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
