<div align="center">

# 🌸 Blossom

**Premium Fashion**

*Combining editorial magazine aesthetics with the power of a real-time full-stack web application*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_v3-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

</div>

---

## About the Project

**Blossom** is a premium e-commerce storefront platform with a modern editorial minimalism aesthetic. Inspired by the luxury boutique visuals of brands such as Zara, Mango, and Vogue, Blossom emphasizes generous whitespace, high-contrast typography blending editorial serif with geometric sans-serif, and a clean flat UI without excessive drop shadows.

Its backend is powered by **Supabase** as the database and real-time authentication system, allowing data changes to be reflected instantly across the interface without requiring a page reload.

---

## ✨ Key Features

### 🛒 Customer Portal

- **Single-Page Hash Routing** — Instant navigation without refreshing the page (`#/`, `#/shop`, `#/product/:id`, `#/wishlist`, `#/cart`, `#/profile`)
- **Product Detail Page (PDP)** — Asymmetric split-screen layout with a large visual gallery, material description, care instructions, and size selection
- **Dynamic Shopping Cart** — Real-time quantity management, automatic coupon calculation, and free shipping for purchases above $75
- **Persistent Wishlist** — Stored directly in the database and retained even after the browser is closed
- **Self-Service Profile Editing** — Update name, email, and password directly from the profile dashboard

### 🛡️ Admin Dashboard

- **Product Management (CRUD)** — Add new collections with images, pricing, discounts, categories, and *Best Seller* labels
- **Real-Time Live Updates** — Every change made on the admin page (`#/admin`) is reflected instantly in the customer catalog
- **Custom Confirmation Modal** — Elegant Blossom-themed confirmation dialog that replaces the default browser dialog

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | HTML5, JavaScript (ES6 Vanilla), Tailwind CSS v3 |
| **Database** | Supabase (PostgreSQL) |
| **Auth & Security** | Supabase Auth + Row Level Security (RLS) |
| **Typography** | Google Fonts — Playfair Display & Inter |

---

## 🗄️ Database Schema

Blossom enables **Row Level Security** on each table to protect user data on the server side.

| Table | Main Columns | RLS Rule |
|---|---|---|
| `profiles` | `id`, `full_name`, `is_admin` | Users can only read and update their own profile |
| `products` | `id`, `name`, `price`, `discount_percent` | Read: public — Write: admin-only |
| `wishlists` | `id`, `user_id`, `product_id` | Only the owner can access |
| `carts` | `id`, `user_id`, `product_id`, `quantity` | Only the owner can access |

---

## 🔒 License

Distributed under the **MIT License**. See the `LICENSE` file for details on commercial use and code distribution.

---

<div align="center">

Developed with dedication to deliver visual luxury and dependable real-time full-stack performance. 🌸

</div>
