# Login Test Cases

## TC_LOGIN_001 — Login with valid credentials

- Username: `standard_user`
- Password: `secret_sauce`
- Expected: Login successful and Products page is displayed.
- Status: PASS

## TC_LOGIN_002 — Login with empty fields

- Username: Empty
- Password: Empty
- Expected: Error message is displayed.
- Status: PASS

## TC_LOGIN_003 — Login with invalid username

- Username: `wrong_user`
- Password: `secret_sauce`
- Expected: Error message is displayed.
- Status: PASS

## TC_LOGIN_004 — Login with invalid password

- Username: `standard_user`
- Password: `wrong_password`
- Expected: Error message is displayed.
- Status: PASS

## TC_LOGIN_005 — Login with locked-out user

- Username: `locked_out_user`
- Password: `secret_sauce`
- Expected: Login is rejected and error message is displayed.
- Status: PASS
  
## Products
**TC_PRODUCT_001 — Verify Products page**

Expected: Products page is displayed with product list.

Status: PASS

**TC_PRODUCT_002 — Sort products by Name A-Z**

Expected: Products are sorted alphabetically from A to Z.

Status: PASS

**TC_PRODUCT_003 — Sort products by Name Z-A**

Expected: Products are sorted alphabetically from Z to A.

Status: PASS

**TC_PRODUCT_004 — Sort products by Price Low-High**

Expected: Products are sorted from lowest to highest price.

Status: PASS

**TC_PRODUCT_005 — Sort products by Price High-Low**

Expected: Products are sorted from highest to lowest price.

Status: PASS

**TC_PRODUCT_006 — Add product to cart**

Expected: Product is added and cart badge is updated.

Status: PASS

**TC_PRODUCT_007 — Add multiple products to cart**

Expected: Selected products are added and cart badge shows the correct count.

Status: PASS

**TC_PRODUCT_008 — Remove product from Products page**

Expected: Product is removed from the cart.

Status: PASS

---

## Cart

**TC_CART_001 — Open Cart**

Expected: Cart page is displayed.

Status: PASS

**TC_CART_002 — Verify added product**

Expected: Added product is displayed with correct name and price.

Status: PASS

**TC_CART_003 — Remove product from Cart**

Expected: Product is removed from the cart.

Status: PASS

**TC_CART_004 — Remove all products**

Expected: Cart becomes empty.

Status: PASS

**TC_CART_005 — Continue Shopping**

Expected: User returns to Products page.

Status: PASS

**TC_CART_006 — Checkout**

Expected: Checkout information page is displayed.

Status: PASS

---

## Checkout

**TC_CHECKOUT_001 — Checkout with empty fields**

First Name: Empty

Last Name: Empty

Zip Code: Empty

Expected: Required field error is displayed.

Status: PASS

**TC_CHECKOUT_002 — Checkout with valid information**

First Name: John

Last Name: Doe

Zip Code: 12345

Expected: User proceeds to Checkout Overview.

Status: PASS

**TC_CHECKOUT_003 — First Name with numeric value**

First Name: 12345

Expected: Application should reject invalid input.

Actual: Invalid input is accepted.

Status: FAIL → BUG

**TC_CHECKOUT_004 — Last Name with special characters**

Last Name: @@@

Expected: Application should reject invalid input.

Actual: Invalid input is accepted.

Status: FAIL → BUG

**TC_CHECKOUT_005 — Zip Code with alphabetic characters**

Zip Code: ABC

Expected: Application should reject invalid input.

Actual: Invalid input is accepted.

Status: FAIL → BUG

**TC_CHECKOUT_006 — Cancel checkout**

Expected: User returns to the Cart page.

Status: PASS

**TC_CHECKOUT_007 — Verify order overview**

Expected: Product, price, subtotal, tax and total are displayed correctly.

Status: PASS

---

## Order

**TC_ORDER_001 — Complete order**

Expected: Order is successfully completed.

Status: PASS

**TC_ORDER_002 — Verify order confirmation message**

Expected: Thank you for your order! is displayed.

Status: PASS

**TC_ORDER_003 — Back Home after order**

Expected: User is redirected to Products page.

Status: PASS

**TC_ORDER_004 — Verify cart after order**

Expected: Cart is empty after completing the order.

Status: PASS

---

## Logout

**TC_LOGOUT_001 — Logout**

Expected: User is redirected to Login page.

Status: PASS

