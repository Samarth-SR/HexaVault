# HexaVault - Password Manager with 2FA

**HexaVault** is a simple, secure password manager that helps users store and manage their passwords safely. The app features a master password authentication system with built-in two-factor authentication (2FA) to enhance security. The app also sends alerts when unauthorized login attempts occur.

## Features

- **Master Password Authentication**: Users authenticate using a master password stored securely with hashing (`bcrypt`).
- **Two-Factor Authentication (2FA)**: A 6-digit code is sent to the user's email after a successful master password login for added security.
- **Failed Login Alerts**: If the maximum login attempts are exceeded, an alert email is sent to notify the user of an unauthorized access attempt.
- **Password Hashing and Salting**: Secure password storage using the `bcrypt` hashing algorithm.
- **Email Notifications**: Sends 2FA codes and alerts using the SMTP protocol.

## Tech Stack

- **Python**: Core language
- **Tkinter**: For GUI
- **bcrypt**: For hashing and verifying passwords
- **smtplib**: For sending emails (2FA codes and alerts)

## Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/hexavault.git
   cd hexavault
   ```

2. **Install dependencies:**

   Ensure `bcrypt` is installed:

   ```bash
   pip install bcrypt
   ```

3. **Configure SMTP settings:**

   Replace the `sender_email` and `sender_password` with your credentials. For Gmail, use an app-specific password.

4. **Run the application:**

   ```bash
   python hexavault.py
   ```

## How It Works

1. The user enters their **master password**.
2. If the password is correct, a **2FA code** is generated and sent to the user’s email.
3. The user must enter the 2FA code to complete the login process.
4. If the password is entered incorrectly multiple times, an **alert email** is sent.

## Contributing

Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.
