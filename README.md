# 🌍 USSD-Pay – Offline Payment System for Real-World Access

**Empowering offline users with secure, simple mobile payments via USSD.**

Built with: **Go + Africa’s Talking + M-Pesa API + PostgreSQL**

---

## 💡 Why This Project?

Millions of people in rural areas and informal economies still don’t have access to smartphones or stable internet—but they need to pay school fees, buy goods, and receive money like everyone else.

**USSD-Pay** enables **feature-phone users** to access digital financial services through a simple dial code like `*123#`.

---

## 🧩 What This System Does

### ✅ For End Users (via USSD):
- Send money to another mobile number
- Pay bills or merchants (e.g. school fees, boda fares)
- Withdraw funds to M-Pesa or Airtel Money
- View transaction history or balance
- Verify actions with PIN

### 🖥️ For Admins (via Dashboard):
- Monitor real-time transactions
- Add merchants and services
- Export payment reports
- Configure services and pricing

---

## ⚙️ Tech Stack

| Component        | Technology Used                       |
|------------------|----------------------------------------|
| USSD Gateway     | Africa’s Talking / Twilio              |
| Backend API      | Go (Golang)                            |
| Mobile Payments  | M-Pesa Daraja API / Flutterwave        |
| Database         | PostgreSQL + Redis                     |
| Auth & Sessions  | JWT + Session Store                    |
| Admin Dashboard  | React + TailwindCSS (or Go Templates)  |
| Hosting          | Render / Railway / Fly.io              |

---

## 🧭 System Architecture

```mermaid
graph TD;
    User -->|USSD Dial| AfricaTalking
    AfricaTalking --> Backend[Go Backend API]
    Backend -->|Send Money| M-PesaAPI
    Backend -->|Record| DB[(PostgreSQL)]
    Admin --> Dashboard[Admin Portal]
    Dashboard --> Backend



