<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechZone Electronics | Online Store</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
    }

    body {
      background: #f4f7fa;
      display: flex;
      justify-content: center;
      padding: 2rem 1rem;
    }

    .page-wrapper {
      max-width: 1200px;
      width: 100%;
      background: white;
      border-radius: 28px;
      box-shadow: 0 20px 40px -12px rgba(0,20,30,0.25);
      overflow: hidden;
    }

    /* header section */
    .store-header {
      background: linear-gradient(145deg, #0b2b3d, #123d4f);
      color: white;
      padding: 2rem 2.5rem 1.5rem 2.5rem;
    }

    .store-header h1 {
      font-size: 2.4rem;
      font-weight: 600;
      letter-spacing: -0.5px;
      margin-bottom: 0.25rem;
    }

    .store-header .tagline {
      font-size: 1rem;
      opacity: 0.85;
      font-weight: 300;
      margin-top: 0.3rem;
    }

    /* navigation bar */
    .nav-bar {
      background: #1e2f3a;
      padding: 0.9rem 2.5rem;
      border-top: 1px solid #31657a;
      border-bottom: 3px solid #ff9f1c;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 2.5rem;
      list-style: none;
    }

    .nav-links a {
      color: #f0f6fc;
      text-decoration: none;
      font-weight: 550;
      font-size: 1.15rem;
      padding: 0.3rem 0;
      border-bottom: 2px solid transparent;
      transition: 0.2s ease;
    }

    .nav-links a:hover {
      border-bottom-color: #ff9f1c;
      color: #ffffff;
    }

    /* main content */
    .main-content {
      padding: 2rem 2.5rem;
    }

    section {
      margin-bottom: 3rem;
    }

    h2 {
      font-size: 2rem;
      font-weight: 550;
      color: #0f3b4c;
      border-left: 7px solid #ff9f1c;
      padding-left: 1.2rem;
      margin-bottom: 1.8rem;
    }

    /* product table */
    .product-table {
      width: 100%;
      border-collapse: collapse;
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 5px 12px rgba(0,0,0,0.08);
    }

    .product-table th {
      background-color: #1f4b5e;
      color: white;
      font-weight: 600;
      font-size: 1.1rem;
      padding: 1rem 0.8rem;
      text-align: left;
    }

    .product-table td {
      background-color: #ffffff;
      padding: 0.9rem 0.8rem;
      border-bottom: 1px solid #d6e2e9;
      color: #132e3a;
    }

    .product-table tr:last-child td {
      border-bottom: none;
    }

    .product-table tr:hover td {
      background-color: #faf1e2;
    }

    /* order form */
    .order-form {
      background: #f9fcff;
      border-radius: 24px;
      padding: 2rem 2rem 2.2rem;
      box-shadow: inset 0 1px 3px #ffffff, 0 12px 24px -16px #123d4f;
      border: 1px solid #d6e2e9;
    }

    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.8rem 2rem;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }

    .form-group.full-width {
      grid-column: 1 / -1;
    }

    label {
      font-weight: 600;
      color: #145369;
      font-size: 1rem;
      letter-spacing: 0.3px;
    }

    input, select, textarea {
      background: white;
      border: 1.5px solid #cbdae3;
      border-radius: 16px;
      padding: 0.8rem 1.2rem;
      font-size: 1rem;
      outline: none;
      transition: 0.15s;
      font-family: inherit;
    }

    input:focus, select:focus, textarea:focus {
      border-color: #ff9f1c;
      box-shadow: 0 0 0 3px rgba(255, 159, 28, 0.2);
    }

    .radio-group {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      align-items: center;
      background: #eef3f8;
      padding: 0.8rem 1.5rem;
      border-radius: 40px;
      border: 1px solid #cde0e9;
    }

    .radio-option {
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .radio-option input[type="radio"] {
      accent-color: #ff9f1c;
      width: 1.2rem;
      height: 1.2rem;
      margin: 0;
    }

    .submit-btn {
      background: #ff9f1c;
      border: none;
      color: #1f2f38;
      font-weight: 700;
      font-size: 1.35rem;
      padding: 1rem 2rem;
      border-radius: 50px;
      cursor: pointer;
      margin-top: 2rem;
      width: 100%;
      border: 2px solid #e58e00;
      transition: 0.2s;
      letter-spacing: 0.5px;
    }

    .submit-btn:hover {
      background: #ffb347;
      border-color: #b36b00;
      transform: scale(1.01);
      box-shadow: 0 8px 18px rgba(255, 159, 28, 0.35);
    }

    /* footer */
    .footer {
      background: #0b2b3d;
      color: #dae9f2;
      padding: 1.8rem 2.5rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      border-top: 4px solid #ff9f1c;
    }

    .footer-email {
      font-size: 1.2rem;
      font-weight: 500;
    }

    .footer-email a {
      color: #ffcf8a;
      text-decoration: none;
      border-bottom: 1px dotted;
    }

    .footer-email a:hover {
      color: white;
      border-bottom: 1px solid white;
    }

    .copyright {
      font-size: 1rem;
      opacity: 0.8;
    }

    /* small extras */
    .ksh-note {
      font-weight: 600;
      color: #1f5e7a;
    }

    /* responsiveness */
    @media (max-width: 750px) {
      .store-header h1 { font-size: 2rem; }
      .nav-links { gap: 1.3rem; }
      .form-grid { grid-template-columns: 1fr; }
      .radio-group { flex-direction: column; align-items: start; gap: 0.8rem; }
      .footer { flex-direction: column; gap: 0.7rem; text-align: center; }
    }
  </style>
</head>
<body>
  <div class="page-wrapper">
    <!-- header -->
    <header class="store-header">
      <h1>TechZone Electronics Online Store</h1>
      <div class="tagline">— innovation at your doorstep 🇰🇪</div>
    </header>

    <!-- navigation -->
    <nav class="nav-bar">
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">Products</a></li>
        <li><a href="#">Order Form</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </nav>

    <!-- main content -->
    <main class="main-content">
      <!-- products table section -->
      <section>
        <h2>📋 available products</h2>
        <table class="product-table">
          <thead>
            <tr>
              <th>Product ID</th>
              <th>Product Name</th>
              <th>Category</th>
              <th>Price (Ksh)</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>P001</td><td>Laptop</td><td>Computers</td><td class="ksh-note">65,000</td></tr>
            <tr><td>P002</td><td>Smartphone</td><td>Mobile Devices</td><td class="ksh-note">32,000</td></tr>
            <tr><td>P003</td><td>Wireless Mouse</td><td>Accessories</td><td class="ksh-note">1,500</td></tr>
            <tr><td>P004</td><td>External Hard Drive</td><td>Storage</td><td class="ksh-note">8,000</td></tr>
          </tbody>
        </table>
        <p style="margin-top: 0.6rem; font-style: italic; color: #375e72;">* all prices inclusive of VAT</p>
      </section>

      <!-- order form section -->
      <section>
        <h2>📝 customer order form</h2>
        <div class="order-form">
          <form action="#" method="post">
            <div class="form-grid">

              <!-- customer name -->
              <div class="form-group">
                <label for="fullname">👤 Full name</label>
                <input type="text" id="fullname" name="fullname" placeholder="e.g. Akinyi Omondi" required>
              </div>

              <!-- email address -->
              <div class="form-group">
                <label for="email">📧 Email address</label>
                <input type="email" id="email" name="email" placeholder="customer@example.com" required>
              </div>

              <!-- product dropdown -->
              <div class="form-group">
                <label for="product">🛒 Select product</label>
                <select id="product" name="product" required>
                  <option value="" disabled selected>– choose an item –</option>
                  <option value="P001 Laptop">Laptop (Ksh 65,000)</option>
                  <option value="P002 Smartphone">Smartphone (Ksh 32,000)</option>
                  <option value="P003 Wireless Mouse">Wireless Mouse (Ksh 1,500)</option>
                  <option value="P004 External Hard Drive">External Hard Drive (Ksh 8,000)</option>
                </select>
              </div>

              <!-- quantity number field -->
              <div class="form-group">
                <label for="quantity">🔢 Quantity</label>
                <input type="number" id="quantity" name="quantity" min="1" value="1" required>
              </div>

              <!-- delivery address (full width) -->
              <div class="form-group full-width">
                <label for="address">🏠 Delivery address</label>
                <textarea id="address" name="address" rows="3" placeholder="Street, building, city, landmark ..." required></textarea>
              </div>

              <!-- payment method - radio group, full width -->
              <div class="form-group full-width">
                <label>💳 Payment method</label>
                <div class="radio-group">
                  <span class="radio-option"><input type="radio" id="mpesa" name="payment" value="M-Pesa" checked> <label for="mpesa">M-Pesa</label></span>
                  <span class="radio-option"><input type="radio" id="card" name="payment" value="Card"> <label for="card">Card</label></span>
                  <span class="radio-option"><input type="radio" id="cash" name="payment" value="Cash on Delivery"> <label for="cash">Cash on Delivery</label></span>
                </div>
              </div>
            </div> <!-- end form-grid -->

            <!-- submit button -->
            <button type="submit" class="submit-btn">✔ place order now</button>
          </form>
        </div>
      </section>
    </main>

    <!-- footer -->
    <footer class="footer">
      <div class="footer-email">
        📬 <a href="mailto:info@techzone.co.ke">info@techzone.co.ke</a>
      </div>
      <div class="copyright">
        © 2025 TechZone Electronics. All rights reserved.
      </div>
    </footer>
  </div>
</body>
</html># index.html2
