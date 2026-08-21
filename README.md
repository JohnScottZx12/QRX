# QRX — Offline-First Optical Data Transfer

<p align="center">
  <strong>Move Data. Without the Network.</strong>
</p>

<p align="center">
  Transfer text, URLs, and files between devices using QR codes.
  <br>
  Designed for offline workflows, controlled data transfer, and exploring optical communication across isolated environments.
</p>

<p align="center">
  <a href="https://johnscottzx12.github.io/QRX/">
    <img src="https://img.shields.io/badge/🚀%20LIVE%20DEMO-Try%20QRX-blue?style=for-the-badge" alt="Live Demo">
  </a>
  <a href="https://github.com/JohnScottZx12/QRX">
    <img src="https://img.shields.io/github/stars/JohnScottZx12/QRX?style=for-the-badge&logo=github" alt="GitHub Stars">
  </a>
  <a href="https://github.com/JohnScottZx12/QRX/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/JohnScottZx12/QRX?style=for-the-badge" alt="License">
  </a>
</p>

---

## 🚀 What is QRX?

**QRX** is a browser-based, offline-first data transfer application that allows users to transfer **text, URLs, and files using QR codes**.

Instead of relying on cloud storage, email, messaging platforms, USB drives, or conventional network connectivity, QRX explores a simple alternative:

```text
Device A → QR Code → Device B
```

QRX uses the **optical channel between a display and a camera** as a data-transfer mechanism. Data can be encoded into QR frames, displayed on one device, captured by another device, validated, reordered when necessary, and reconstructed.

This makes QRX useful for exploring:

* Offline data transfer
* QR-based file transfer
* Controlled data movement
* Isolated environments
* Air-gapped system workflows
* Optical communication concepts

> **QRX explores how QR codes can be used as a practical optical data-transfer layer between devices.**

---

## 🌐 Live Demo

### [🚀 Launch QRX](https://johnscottzx12.github.io/QRX/)

QRX runs directly in the browser, so there is no traditional application installation required.

**Try it:**
https://johnscottzx12.github.io/QRX/

---

# ✨ Key Features

## 📦 Transfer Text, URLs & Files

QRX supports multiple types of data:

* 📝 Text
* 🔗 URLs
* 📁 Files

The application converts the selected data into a QR-based transfer format that can be captured and reconstructed by the receiving device.

---

## 🔄 Out-of-Order QR Reconstruction

Larger transfers may require multiple QR frames.

QRX does **not require the QR frames to be scanned strictly in sequence**.

For example, a transfer such as:

```text
QR 1 → QR 2 → QR 3 → QR 4 → QR 5
```

can be captured in an order such as:

```text
QR 4 → QR 1 → QR 5 → QR 2 → QR 3
```

QRX can identify the individual frames and reconstruct the transfer in the correct order.

This is particularly useful when scanning multiple QR frames manually or when frames are captured at different times.

---

## ✅ Transfer Validation & Integrity Checking

QRX validates received QR data before attempting to reconstruct the final output.

The application can identify whether received QR frames belong to the expected transfer and whether the required transfer information is valid.

This helps prevent unrelated, invalid, incomplete, or corrupted QR data from being incorrectly treated as part of the current transfer.

> **Transfer validation is an important part of making multi-frame optical data transfer reliable.**

---

## 🔐 Password-Protected Transfers

QRX supports **password-protected QR transfers**.

A password can be used to protect the transfer payload and add an additional layer of access control.

This can be useful when QR data is being transferred in an environment where someone other than the intended recipient could potentially observe or capture the QR frames.

> Password protection should be considered one component of a broader security model and should not, by itself, be treated as a guarantee of secure communication.

---

## 🌐 Universal QR Generator

QRX includes a **Universal QR** generation mode designed for interoperability with standard QR scanners.

This is useful when the receiving device does not have QRX available or when you simply want to generate QR-compatible data that can be read using a conventional QR-scanning application.

In other words:

```text
                 QRX
                  │
        ┌─────────┴─────────┐
        │                   │
        ▼                   ▼
 QRX Transfer Mode    Universal QR Mode
        │                   │
        ▼                   ▼
 QRX-to-QRX workflow   Standard QR scanners
```

This gives QRX two different approaches:

**QRX Transfer Mode**
For structured QR-based data transfer between QRX-enabled devices.

**Universal QR Mode**
For generating QR codes intended to work with standard QR scanners.

---

## 📴 Offline-First

QRX is designed around an offline-first workflow.

The optical transfer itself does not require the sending and receiving devices to establish a conventional network connection.

This makes QRX interesting for environments where network connectivity is unavailable, undesirable, or intentionally restricted.

---

## 💻 Browser-Based

QRX runs directly in a modern web browser.

No traditional application installation is required for the web application.

This also makes it easy to deploy as a static web application.

---

## 🔒 Local Processing

QRX is designed around client-side browser processing for its core workflow.

The transfer mechanism does not require the user's data to be uploaded to a cloud storage service.

This can be useful when users want to avoid placing transferred information on third-party infrastructure.

---

# 📸 Screenshots

QRX is designed with a simple interface focused on creating, scanning, validating, and reconstructing QR-based transfers.

<p align="center">
  <em>Open the <a href="https://johnscottzx12.github.io/QRX/">Live Demo</a> to explore the application.</em>
</p>

---

# 🔐 Air-Gapped Systems

One of the most interesting potential applications of QRX is **controlled data transfer between air-gapped systems**.

An air-gapped system is intentionally isolated from conventional networks to reduce its exposure to external network-based threats.

However, isolation introduces a practical challenge:

> **How can necessary information be moved into or out of an isolated environment without connecting the system to a conventional network?**

QRX explores one possible approach using **optical data transfer through QR codes**.

## Optical Transfer Concept

```text
┌──────────────────────┐                 ┌──────────────────────┐
│   AIR-GAPPED SYSTEM  │                 │   RECEIVING SYSTEM   │
│                      │                 │                      │
│      Data / File     │                 │       Camera         │
│          │           │                 │          │           │
│          ▼           │                 │          ▼           │
│    QRX Encoder       │                 │     QRX Decoder      │
│          │           │                 │          │           │
│          ▼           │                 │          ▼           │
│    QR on Display     │ ── OPTICAL ──► │   Reconstructed Data  │
│                      │     CHANNEL     │                      │
└──────────────────────┘                 └──────────────────────┘

        No Wi-Fi • No Bluetooth • No Network
```

The sending system displays the QR data while the receiving system captures it using a camera.

The two systems can therefore communicate through a **visual/optical channel**, without requiring a conventional network connection between them.

---

# 🛡️ Potential Air-Gapped Use Cases

QRX could potentially be incorporated into controlled environments such as:

* 🖥️ Air-gapped workstations
* 🏭 Industrial control environments
* 🧪 Research and laboratory systems
* 🏢 Restricted or isolated networks
* 🔑 Configuration transfer
* 📄 Transfer of small documents or text data
* 💾 Offline system provisioning
* 📡 One-way data export workflows
* 🔐 Controlled movement of information across isolated environments

The suitability of QRX for a particular environment depends on the security requirements, threat model, payload type, and operational controls surrounding the system.

---

# ⚙️ How QRX Works

The basic transfer workflow can be summarized as:

```text
          SENDER
             │
             ▼
     ┌──────────────┐
     │  Input Data  │
     │ Text/File/URL│
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │ Encode Data  │
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │ Split Into   │
     │ QR Frames    │
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │ Add Transfer │
     │ Information  │
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │ QR Generator │
     └──────┬───────┘
            │
            ▼
     ╔══════════════╗
     ║   OPTICAL    ║
     ║    CHANNEL   ║
     ╚══════╤═══════╝
            │
            ▼
     ┌──────────────┐
     │ QR Scanner   │
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │   Validate   │
     │ QR Transfer  │
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │ Reorder QR   │
     │    Frames    │
     └──────┬───────┘
            │
            ▼
     ┌──────────────┐
     │ Reconstruct  │
     │ Original Data│
     └──────┬───────┘
            │
            ▼
          RECEIVER
```

For multi-frame transfers, QRX can identify the individual frames and reconstruct the original data even when the frames are received out of order.

---

# 🧠 Why QR Codes?

QR codes provide an interesting bridge between the **digital and physical worlds**.

A device can:

1. Convert digital information into QR data.
2. Display that information visually.
3. Allow another device to capture it with a camera.
4. Decode and reconstruct the original information.

Conceptually:

```text
Digital Data
     │
     ▼
QR Encoding
     │
     ▼
Visual / Optical Channel
     │
     ▼
Camera
     │
     ▼
QR Decoding
     │
     ▼
Transfer Validation
     │
     ▼
Frame Reordering
     │
     ▼
Original Data
```

This makes QR codes an interesting medium for experimenting with **offline communication and optical data transfer**.

---

# 🔒 Security & Privacy

QRX is designed around a **local-first browser processing model**.

The core workflow does not require uploading transferred data to a cloud storage service.

Security-related features include:

* 🔐 Password-protected transfers
* ✅ Transfer validation
* 🔄 Out-of-order frame reconstruction
* 📴 Offline-first operation
* 🔒 Client-side processing
* 📡 Optical transfer without a conventional network connection
* 🌐 Universal QR generation

## ⚠️ Security Disclaimer

**QRX is a data-transfer mechanism, not a complete security solution.**

An air-gapped environment is not automatically secure simply because it has no network connection.

For real-world high-security deployments, additional controls may be required depending on the threat model, including:

* Strong encryption
* Cryptographic integrity verification
* Sender and receiver authentication
* Malware scanning
* Payload validation
* Audit logging
* Human approval of transfers
* Physical security
* Secure operating-system configuration
* Secure handling of passwords and keys

A compromised sending system could still generate malicious data and encode it into QR frames.

Similarly, a receiving system must still treat transferred files and data as potentially untrusted.

> **QRX does not claim to make an air-gapped system secure by itself. It provides a controlled optical mechanism that can be incorporated into a broader security architecture.**

---

# 🎯 Example Use Cases

### 📴 Offline Data Transfer

Move information between devices without depending on conventional network connectivity.

### 🔐 Air-Gapped Environments

Explore controlled optical data transfer between isolated systems.

### 🧪 Security Research

Experiment with QR codes as an optical communication and data-transfer mechanism.

### 💻 Developer Workflows

Transfer URLs, configuration information, text, or small files between devices.

### 🏢 Restricted Environments

Provide an alternative transfer mechanism where conventional network connectivity is unavailable or intentionally restricted.

---

# 🛠️ Technology

QRX is built using standard web technologies.

| Technology       | Purpose                                 |
| ---------------- | --------------------------------------- |
| **HTML5**        | Application structure                   |
| **CSS3**         | Interface and responsive design         |
| **JavaScript**   | Application logic and transfer workflow |
| **QR Libraries** | QR generation and decoding              |
| **Browser APIs** | Client-side browser functionality       |

The application can be deployed as a static web application.

---

# 📂 Project Structure

```text
QRX/
│
├── index.html
├── script.js
├── style.css
│
├── js/
│   └── ...
│
├── vendor/
│   └── ...
│
├── LICENSE
└── README.md
```

---

# 🚀 Getting Started

## Clone the Repository

```bash
git clone https://github.com/JohnScottZx12/QRX.git
```

## Enter the Project Directory

```bash
cd QRX
```

## Run Locally

QRX can be served using any static web server.

For example, using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

You can also run the project using **Live Server** in Visual Studio Code.

---

# 🌍 Deployment

QRX is a browser-based application and can be deployed using static hosting.

The current live deployment is available at:

### 🚀 https://johnscottzx12.github.io/QRX/

Because the application can run as a static web application, it can also be hosted locally in environments where internet access is unavailable or intentionally restricted.

---

# 🤝 Contributing

Contributions, ideas, bug reports, and suggestions are welcome.

If you find a problem or have an idea for improving QRX:

1. Open an **Issue**
2. Describe the problem or proposed improvement
3. Submit a **Pull Request** if you have implemented a solution

Please keep security-related discussions responsible and avoid publishing sensitive information or exploitable details.

---

# 📜 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](./LICENSE) file for details.

---

# ⭐ Support QRX

If you find QRX interesting or useful, consider supporting the project:

⭐ **Star the repository**

🐛 **Report bugs**

💡 **Share ideas**

🔀 **Contribute improvements**

Every star and contribution helps QRX reach more developers and security enthusiasts.

---

<p align="center">

## QRX

<strong>Move Data. Without the Network.</strong>

Built with ❤️ using the web platform.

</p>
