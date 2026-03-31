Here’s a clean and professional **README.md** you can use for your project 👇

---

# 🔍 Network Port Scanner (Tkinter GUI)

A simple, fast, and lightweight **multi-threaded port scanner** with a minimal GUI built using Python and Tkinter.

This tool allows you to scan a target host for open ports within a specified range and view results in real time.

---

## 🚀 Features

* ✅ Multi-threaded scanning (fast performance)
* ✅ Minimal and user-friendly GUI
* ✅ Real-time progress updates
* ✅ Displays open ports with common service names
* ✅ Stop scan anytime
* ✅ Save results to a file
* ✅ Automatic hostname resolution

---

## 🖥 GUI Overview

**Inputs:**

* Target (IP address or hostname)
* Start Port
* End Port

**Outputs:**

* Live scan results
* Progress bar
* Elapsed time
* Open ports list

---

## 📦 Requirements

* Python 3.7+
* Standard libraries only (no external dependencies)

---

## ▶ How to Run

1. Clone or download the project
2. Open terminal / command prompt
3. Run the script:

```bash
python scanner.py
```

---

## 🛠 How It Works

* Uses Python’s `socket` module to attempt TCP connections
* Each port is scanned in a separate thread (controlled via semaphore)
* Open ports are detected when `connect_ex()` returns `0`
* Results are pushed to a thread-safe queue and displayed in GUI

---

## ⚙ Default Internal Settings

| Setting     | Value   |
| ----------- | ------- |
| Timeout     | 0.5 sec |
| Max Threads | 500     |

*(These are not exposed in GUI but can be modified in code.)*

---

## 📄 Output Example

```
Target: example.com (93.184.216.34)
Range: 1-1024

[+] Port 80 (HTTP) is open
[+] Port 443 (HTTPS) is open

Scan complete.
Open ports found: 2
```

---

## 💾 Saving Results

* Click **"Save Results"**
* Choose file location
* Results are saved as `.txt`

---

## ⚠ Important Notes

* 🔐 Only scan systems you own or have permission to test
* 🚫 Unauthorized scanning may be illegal
* 🛡 Some systems may block or rate-limit scanning

---

## 🧩 Customization

You can extend the scanner easily:

### Add More Services

Edit the `COMMON_PORTS` dictionary:

```python
COMMON_PORTS = {
    21: 'FTP',
    22: 'SSH',
    ...
}
```

### Adjust Speed

Modify:

```python
timeout = 0.5
max_threads = 500
```

---

## 🐞 Known Limitations

* Only TCP connect scan (no SYN scan)
* No OS detection
* No UDP scanning
* High thread count may affect low-end systems

---

## 📌 Future Improvements

* [ ] Add UDP scanning
* [ ] Add banner grabbing
* [ ] Export to CSV/JSON
* [ ] Dark mode UI
* [ ] Custom thread/timeout settings in GUI

---

## 📜 License

This project is open-source and free to use for educational purposes.

---

## 🙌 Acknowledgements

Built using:

* Python `socket`
* `threading`
* `tkinter`

## Output
<img width="902" height="690" alt="image" src="https://github.com/user-attachments/assets/364e4c65-caaf-4dfc-becd-24a6ebe27429" />

---
