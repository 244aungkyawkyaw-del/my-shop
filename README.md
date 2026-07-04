<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Online Shop</title>
    <style>
        body { font-family: sans-serif; background-color: #f4f4f9; text-align: center; padding: 20px; }
        .container { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-top: 20px; }
        .product-card { background: white; border-radius: 10px; padding: 20px; width: 280px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        .product-card img { max-width: 100%; border-radius: 8px; }
        .btn { background-color: #007bff; color: white; padding: 10px; border: none; width: 100%; border-radius: 5px; margin-top: 10px; cursor: pointer; }
        .order-form { max-width: 400px; margin: 40px auto; background: white; padding: 20px; border-radius: 10px; text-align: left; }
        input, textarea, select { width: 100%; padding: 8px; margin: 10px 0; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box; }
        .submit-btn { background-color: #28a745; color: white; padding: 10px; border: none; width: 100%; font-weight: bold; }
    </style>
</head>
<body>
    <h1>Welcome to My Online Shop 🚀</h1>
    <div class="container">
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1695048133142-1a20484d2569?w=500" alt="iPhone 16">
            <h3>iPhone 16 Pro Max</h3>
            <p>ဈေးနှုန်း - $1,200</p>
            <button class="btn" onclick="selectProduct('iPhone 16 Pro Max')">ချက်ချင်းဝယ်ယူမည်</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1542496658-e33a6d0d50f6?w=500" alt="Apple Watch">
            <h3>Apple Watch Ultra</h3>
            <p>ဈေးနှုန်း - $799</p>
            <button class="btn" onclick="selectProduct('Apple Watch Ultra')">ချက်ချင်းဝယ်ယူမည်</button>
        </div>
    </div>
    <div class="order-form" id="order-form">
        <h2>🛍️ ပစ္စည်းမှာယူရန်</h2>
        <select id="product"><option value="iPhone 16 Pro Max">iPhone 16 Pro Max</option><option value="Apple Watch Ultra">Apple Watch Ultra</option></select>
        <input type="text" id="name" placeholder="အမည်">
        <input type="text" id="phone" placeholder="ဖုန်းနံပါတ်">
        <textarea id="address" placeholder="လိပ်စာ"></textarea>
        <button class="submit-btn" onclick="sendOrder()">Messenger သို့ ပို့မည် 💬</button>
    </div>
    <script>
        function selectProduct(p) { document.getElementById('product').value = p; document.getElementById('order-form').scrollIntoView(); }
        function sendOrder() {
            const p = document.getElementById('product').value, n = document.getElementById('name').value, ph = document.getElementById('phone').value, a = document.getElementById('address').value;
            const msg = `အော်ဒါအသစ်-%0Aပစ္စည်း: ${p}%0Aအမည်: ${n}%0Aဖုန်း: ${ph}%0Aလိပ်စာ: ${a}`;
            window.open(`https://m.me/me?text=${msg}`, '_blank');
        }
    </script>
</body>
</html>
