# ShopNow Ecommerce Platform

A Django-based ecommerce platform that allows users to browse products, add items to their cart, and complete orders through a checkout process. This project supports user authentication, guest checkout functionality, and utilizes AJAX for dynamic cart updates.

## Features

- **Product Display:** Showcase products with images, prices, and names.
- **Cart Functionality:** Dynamically add, remove, and update product quantities.
- **Checkout Process:** Capture shipping information and process orders.
- **User Authentication:** Login, registration, and guest checkout support.
- **Admin Interface:** Manage products, orders, customers, and shipping details.
- **Responsive Design:** Mobile-friendly interfaces built using Bootstrap.

## Project Structure

```
Ecommerce/
├── Ecommerce/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── __pycache__/
├── static/
│   ├── css/
│   │   └── main.css
│   ├── images/
│   │   ├── cart.png
│   │   ├── arrow-down.png
│   │   ├── arrow-up.png
│   │   └── ... (more images)
│   └── js/
│       └── cart.js
├── store/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── signals.py
│   ├── tests.py
│   ├── urls.py
│   ├── utils.py
│   ├── views.py
│   └── Templates/
│       └── store/
│           ├── cart.html
│           ├── checkout.html
│           ├── login.html
│           ├── main.html
│           └── store.html
├── db.sqlite3
├── manage.py
├── backup.json
└── Readme.md  (alternate readme file)
```

## Installation

1. **Clone the Repository**

   ```sh
   git clone https://github.com/Ranuva-NIKHIL-Rao/ShopNow.git
   cd ecommerce-platform
   ```

2. **Create and Activate Virtual Environment**

   ```sh
   python -m venv venv
   # On Mac/Linux:
   source venv/bin/activate
   # On Windows:
   venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```sh
   pip install -r requirements.txt
   ```

4. **Apply Migrations**

   ```sh
   python manage.py migrate
   ```

5. **Create a Superuser for the Admin Interface**

   ```sh
   python manage.py createsuperuser
   ```

6. **Run the Development Server**
   ```sh
   python manage.py runserver
   ```
   Open your browser at `http://127.0.0.1:8000` to access the storefront.

## Usage

- **Storefront:** Browse available products on the home page. Click "Add to Cart" to update your order.
- **Cart:** Review your selected items and update quantities directly on the cart page.
- **Checkout:** Fill in your shipping and payment details on the checkout form.
- **User Authentication:** Use the login page at `/login` to sign in or register as a new user.
- **Admin Panel:** Access `/admin` for managing products, orders, and customer details.

## Customization

- **Static Files:** Modify the CSS [`static/css/main.css`] and JavaScript [`static/js/cart.js`] files to change the UI.
- **Templates:** Edit the HTML templates in the [`store/Templates/store/`] directory.
- **Django Settings:** Update configuration in [`Ecommerce/settings.py`] for static paths, debugging, and more.

## Screenshots

![Home Page](/Screenshots/sn.png)
![Cart Page](/Screenshots/snc.png)
![Checkout Page](/Screenshots/snca.png)
![Payment using Payapal](/Screenshots/snp.png)

## Development & Testing

- Run Django’s test suite:
  ```sh
  python manage.py test store
  ```

## Deployment

Before deploying to production:

- Set `DEBUG = False` in [`Ecommerce/settings.py`].
- Configure `ALLOWED_HOSTS` appropriately.
- Set up a proper hosting solution for static files and media.

## Backup & Data

- A sample backup file is located at [`backup.json`]which contains initial data for products and user actions.

## Contributing

Contributions are welcome! Fork the repository and create a pull request with your changes. Please follow the existing code style and include tests where necessary.
