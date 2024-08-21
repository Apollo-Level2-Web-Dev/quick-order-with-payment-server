# Quick Order Server

This repository contains the backend for a quick order system, fully integrated with the AmarPay payment gateway. It is designed specifically for educational purposes in the Next Level Web Development course, demonstrating how to implement payment processing in a server-side application.

---

### **Directory Structure**

```plaintext
src/
├── app/                     # Core application logic
│   ├── config/              # Configuration files
│   │   ├── db.ts            # Database configuration
│   │   └── seed.ts          # Data seeding script
│   └── modules/             # Application modules (e.g., order, payment, product)
│       ├── order/           # Order module
│       │   ├── order.controller.ts   # Controller for order-related routes
│       │   ├── order.model.ts        # Mongoose model for orders
│       │   ├── order.routes.ts       # Routes for order-related endpoints
│       │   └── order.service.ts      # Service layer for order logic
│       ├── payment/         # Payment module
│       │   ├── payment.controller.ts # Controller for payment-related routes
│       │   ├── payment.route.ts      # Routes for payment-related endpoints
│       │   ├── payment.service.ts    # Service layer for payment logic
│       │   └── payment.utils.ts      # Utility functions for payment processing
│       └── product/         # Product module
│           ├── product.controller.ts # Controller for product-related routes
│           ├── product.model.ts      # Mongoose model for products
│           ├── product.routes.ts     # Routes for product-related endpoints
│           └── product.service.ts    # Service layer for product logic
├── views/                   # HTML templates for views
│   └── confirmation.html    # Payment confirmation view
├── app.ts                   # Main application entry point
└── index.ts                 # Server initialization
.env                         # Environment variables
```

---

### **Environment Variables**

Your `.env` file should be set up as follows:

```plaintext
DB_URL="YOUR DB URL"
PORT=3000
STORE_ID="aamarpaytest"
SIGNETURE_KEY="dbb74894e82415a2f7ff0ec3a97e4183"
PAYMENT_URL="https://sandbox.aamarpay.com/jsonpost.php"
PAYMENT_VERIFY_URL="https://sandbox.aamarpay.com/api/v1/trxcheck/request.php"
```

- **`DB_URL`**: The connection string for your MongoDB database.
- **`PORT`**: The port on which the server will run.
- **`STORE_ID`**: Your AmarPay store ID.
- **`SIGNETURE_KEY`**: Your AmarPay signature key.
- **`PAYMENT_URL`**: The URL for initiating payments with AmarPay.
- **`PAYMENT_VERIFY_URL`**: The URL for verifying payment transactions.

---

### **Getting Started**

To get started with this project, follow these steps:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Apollo-Level2-Web-Dev/quick-order-with-payment-server.git
   ```

2. **Navigate to the Project Directory:**

   ```bash
   cd quick-order-server
   ```

3. **Install Dependencies:**

   Ensure you have Node.js installed. Then run the following command to install the required dependencies:

   ```bash
   npm install
   ```

4. **Set Up Environment Variables:**

   Create a `.env` file in the root of your project directory with the provided environment variables.

5. **Run the Development Server:**

   Start the development server with:

   ```bash
   npm run dev
   ```

   The server will be available at `http://localhost:3000` (or your configured port).

---

### **Important Links**

- [AmarPay](https://www.aamarpay.com/)
- [Initiate Payment (JSON)](https://aamarpay.readme.io/reference/initiate-payment-json)
- [Search Transaction](https://aamarpay.readme.io/reference/search-transaction)

---

This project demonstrates a complete backend solution for create orders with online payment, integrating seamlessly with the AmarPay payment gateway.