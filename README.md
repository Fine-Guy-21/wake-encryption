# 🔐 Word Auto-Key Encryption (WAKE) Web App

A web-based cryptography tool built with **[Anvil](https://anvil.works)** that demonstrates the **Word Auto-Key Encryption (WAKE)** stream cipher algorithm. Developed as an academic information security project, this application lets users interactively encrypt and decrypt messages using pure Python.

🌐 **Live Demo:** [delirious-shocking-money.anvil.app](https://anvil.app)

---

## 📜 About WAKE & History

**Word Auto-Key Encryption (WAKE)** is a symmetric-key stream cipher designed by computer scientist **David Wheeler** in **1993** (and presented at the *Fast Software Encryption* workshop). Wheeler—co-creator of the Burrows-Wheeler transform and the Tiny Encryption Algorithm (TEA)—designed WAKE specifically to achieve high-speed encryption on 32-bit general-purpose processors.

### How It Works
* **32-Bit Word Architecture:** Unlike classic ciphers that operate on single bits or bytes, WAKE processes data in **32-bit words** using a **128-bit secret key** and a **256 × 32-bit substitution box (S-box)**.
* **Cipher Feedback (Auto-Key) Mode:** WAKE generates its keystream dynamically by feeding previously generated ciphertext words back into the internal state alongside bitwise `XOR`, `AND`, `OR`, and right-shift operations.
* **Cryptanalytic History:** While prized in the 1990s for its software speed and simplicity, subsequent cryptanalysis revealed that WAKE is vulnerable to **chosen-plaintext** and **chosen-ciphertext attacks**. As a result, it serves today as a classic educational model for studying stream cipher mechanics rather than a production security standard.

---

## 🚀 How to Clone & Run the Project

You can run this project either inside the **Anvil Cloud IDE** or locally on your machine using the open-source **Anvil App Server**.

### Option 1: Clone & Run in Anvil (Cloud IDE)
1. Sign in to your [Anvil Works](https://anvil.works) account.
2. Open the **Anvil Editor**, click **New Blank App** (or open your dashboard), and go to **Version Control** (the Git icon in the left sidebar).
3. Select **Clone from Git** and paste your repository URL:
   ```text
   https://github.com/<your-username>/<your-repo-name>.git
   ```
4. Once imported, click **Run** in the top-right toolbar to launch the application.

### Option 2: Clone & Run Locally (Anvil App Server)
Make sure you have **Python 3** and **Java (JDK 8 or higher)** installed on your system, as the Anvil runtime requires Java to serve the backend.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

2. **Create and activate a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install the Anvil App Server:**
   ```bash
   pip install anvil-app-server
   ```

4. **Start the application:**
   ```bash
   anvil-app-server --app .
   ```
5. Open your browser and navigate to `http://localhost:3030` to use the app.

---

## 🛠️ Tech Stack

* **Frontend & Backend Framework:** [Anvil](https://anvil.works) (Pure Python Web Framework)
* **Language:** Python 3
* **Algorithm:** Word Auto-Key Encryption (WAKE)

---

## ⚠️ Educational Disclaimer

This project was built for **academic and educational demonstration purposes**. Because WAKE has documented vulnerabilities against chosen-plaintext/ciphertext attacks, it should **not** be used to protect sensitive or production data. For modern encryption needs, use **AES-GCM** or **ChaCha20-Poly1305**.

---

## 📄 License

Distributed under the [MIT License](LICENSE).
