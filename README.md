# 🏨 Hotel Booking System

A simple Python-based hotel reservation system that allows users to:

- View hotel availability
- Book hotels
- Validate credit card information
- Authenticate secure payments
- Generate reservation confirmations

Built using **Python** and **Pandas**.

---

## 🚀 Features

✅ Load hotel and payment data from CSV files  
✅ Check hotel availability  
✅ Book hotels and update availability  
✅ Validate customer credit card information  
✅ Authenticate secure credit card payments  
✅ Generate reservation receipts  

---

## 🛠️ Technologies Used

- Python 3
- Pandas
- CSV data storage
- Object-Oriented Programming (OOP)

---

## 📂 Project Structure

```bash
.
├── main.py
├── hotels.csv
├── cards.csv
├── card_security.csv
└── README.md
```

---

## 📋 CSV Files

### `hotels.csv`

Stores hotel information and availability.

| id | name | available |
|----|------|-----------|
| 101 | Hilton Hotel | yes |

---

### `cards.csv`

Stores valid payment card data.

| number | expiration | holder | cvc |
|--------|------------|--------|-----|

---

### `card_security.csv`

Stores card authentication passwords.

| number | password |
|--------|----------|

---

## ⚙️ How It Works

### 1️⃣ Load Data

The application loads hotel and payment data using Pandas:

```python
df = pandas.read_csv("hotels.csv", dtype={"id": str})
```

---

### 2️⃣ Hotel Availability

The `Hotel` class checks whether a hotel is available.

```python
hotel.available()
```

If available, the hotel can be booked.

---

### 3️⃣ Payment Validation

The `CreditCard` class validates:

- Card number
- Expiration date
- Card holder
- CVC

```python
credit_card.validate(expiration, holder, cvc)
```

---

### 4️⃣ Secure Authentication

The `SecureCreditCard` class adds password authentication.

```python
credit_card.authenticate(given_password)
```

---

### 5️⃣ Reservation Confirmation

A reservation receipt is generated after successful booking.

Example:

```text
Thank you for your reservation!

Here are the booking data:
Name: John Doe
Hotel name: Hilton Hotel
```

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-repo-url>
```

### 2. Navigate to the project folder

```bash
cd hotel-booking-system
```

### 3. Install dependencies

```bash
pip install pandas
```

### 4. Run the program

```bash
python main.py
```

---

## 🧠 OOP Concepts Used

This project demonstrates:

- Classes and objects
- Inheritance
- Encapsulation
- Method overriding
- Composition

---

## 📈 Class Overview

### `Hotel`

Handles:
- Hotel information
- Availability checks
- Booking logic

### `Reservation`

Handles:
- Reservation generation
- Customer booking details

### `CreditCard`

Handles:
- Payment validation

### `SecureCreditCard`

Extends `CreditCard` with:
- Password authentication

---

## ⚠️ Known Issues

There is a small typo bug in the authentication method:

```python
df-df_cards_security
```

Should be:

```python
df_cards_security
```

Correct version:

```python
password = df_cards_security.loc[
    df_cards_security["number"] == self.number,
    "password"
].squeeze()
```

---

## 💡 Future Improvements

- Add GUI interface
- Store reservations in a database
- Encrypt passwords
- Add cancellation feature
- Support multiple room bookings
- Add unit tests

---

## 📸 Example Console Output

```bash
Enter hotel id: 101
Please provide your card number:
Enter your name: John Doe

Thank you for your reservation!
Here are the booking data:
Name: John Doe
Hotel name: Hilton Hotel
```

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a new branch
3. Commit your changes
4. Open a pull request

---

## 📜 License

This project is for educational purposes only.

---

## ⭐ Support

If you found this project helpful, give it a ⭐ on GitHub!



Adding a venv 
```
py -m venv venv
```
Activating for Powershell
```
.\venv\Scripts\Activate.ps1
```


