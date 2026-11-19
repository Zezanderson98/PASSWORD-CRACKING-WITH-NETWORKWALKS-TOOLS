# NETWORKWALKS-B084-WK3-PM2-PASSWORD-CRACKING-WITH-NETWORKWALKS-TOOLS



<div align="center">

# 🔐 Penetration Testing Lab : Password Cracking with Networkwalks Tools

**Extracting Cryptographic PDF Hashes & Auditing Password Strength with Networkwalks Tools**
</div>

<p align="center">
<img width="118" height="20" alt="image" src="https://github.com/user-attachments/assets/c7f8b072-f2a5-445f-b741-8e9b5ae3d638" />
<img width="99" height="20" alt="image" src="https://github.com/user-attachments/assets/b2ad8ab5-760b-4c0e-904f-6325e0ad06fd" />
<img width="141" height="20" alt="image" src="https://github.com/user-attachments/assets/1632e17a-962d-49e7-8280-0eccf09403b1" />
<img width="71" height="20" alt="image" src="https://github.com/user-attachments/assets/ba32250a-4556-4c8a-ba4e-76547de2b868" />
<img width="119" height="20" alt="image" src="https://github.com/user-attachments/assets/b1ee05d4-585b-4232-bc86-4e86c2a0e487" />
<img width="162" height="20" alt="image" src="https://github.com/user-attachments/assets/54057d7d-4f04-4275-8d76-5d416c198555" />

<img width="182" height="20" alt="image" src="https://github.com/user-attachments/assets/b6114453-4092-420e-8536-e225e03cd225" />

<img width="182" height="20" alt="image" src="https://github.com/user-attachments/assets/2c0921f0-59eb-40f4-8216-43c5fa5e6546" />

<img width="171" height="20" alt="image" src="https://github.com/user-attachments/assets/6bb56a6b-63b0-42a8-b92e-2d554e4044d7" />














## 📌 Project Overview
This project demonstrates how to extract cryptographic hashes and recover weak passwords from encrypted PDF files using browser-based security utilities developed by **NetworkWalks**: the **Hash Calculator** and the **Password Cracker**. Because both utilities operate directly inside a web browser with local client-side parsing, security professionals and students can perform hash extraction and dictionary attacks across Windows, Linux, or macOS without installing local binaries.

---

## 🎯 Purpose of the Lab
The purpose of this laboratory exercise is to demonstrate the mechanics of password auditing and dictionary-based credential recovery in a controlled environment. By extracting a `$pdf$` hash from a password-protected document and running an automated wordlist attack, this lab highlights how quickly weak or common passwords are compromised and reinforces strong password security practices.

---

## 🚀 Objectives
* **Understand Password Auditing:** Learn how password recovery works step-by-step from hash extraction to plaintext verification.
* **Differentiate Encryption vs. Hashing:** Distinguish between reversible two-way encryption and irreversible one-way cryptographic hashing.
* **Browser-Based Hash Extraction:** Extract a crackable `$pdf$` hash string from an encrypted PDF (`My Locked PDF1.pdf`) using the NetworkWalks Hash Calculator.
* **Dictionary Attack Execution:** Execute a wordlist-driven password attack using the NetworkWalks Password Cracker.
* **Security Awareness & Defense:** Analyze the vulnerability of short, predictable passwords and apply effective defensive mitigations.

---

## 🏗️ Lab Architecture & Environment
* **Operating System:** Windows 10 PRO
* **Hash Extraction Utility:** <https://networkwalks.com/hash-calculator> (client-side PDF hash parser)
* **Password Cracking Utility:** <https://networkwalks.com/password-cracker/> (browser-based dictionary attack engine)
* **Target Asset:** `My Locked PDF1.pdf` (Password-protected PDF document)

```mermaid
flowchart LR
    A[Encrypted PDF<br/>My Locked PDF1.pdf] -->|Load Local File| B[NetworkWalks Hash Calculator<br/>Browser Parser]
    B -->|Extract pdf Hash| C[Cryptographic PDF Hash<br/>pdf2john / hashcat format]
    C -->|Copy & Paste Hash| D[NetworkWalks Password Cracker<br/>Dictionary Attack Engine]
    D -->|Wordlist Matching| E[Recovered Plaintext Password<br/>password1]
    E -->|Unlock Document| F[Access Granted / Flag Captured]
```

---

## 🛠️ Step-by-Step Lab Tasks

### 1. Download the Encrypted Target PDF
* Download the target encrypted file <https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/>  to your local workstation.


<img width="1366" height="768" alt="1_download encrypted pdf1 file" src="https://github.com/user-attachments/assets/778808da-a543-4fe7-8140-08ab5e1aa382" />









### 2. Open the NetworkWalks Hash Calculator
* Launch your web browser and navigate to the <https://networkwalks.com/hash-calculator/>
* Select the **PDF** tab to prepare for file hash extraction.



<img width="1363" height="768" alt="2_open networkwalks hash calculator" src="https://github.com/user-attachments/assets/564ca320-06e4-487e-a68b-b1c51ccf2f04" />








### 3. Upload the Locked PDF File
* Click to choose or drag and drop `My Locked PDF1.pdf` into the Hash Calculator.
* The tool parses the file locally and extracts the cryptographic hash string starting with `$pdf$...`.



<img width="1364" height="768" alt="3_upload pdf1 file to hash calculator" src="https://github.com/user-attachments/assets/ffa955ad-1949-4e91-8ba4-8f2c6d26c8a1" />










### 4. Copy the Complete Extracted Hash
* Click **Copy** (or manually highlight and copy) the full generated hash output.
  > **Note:** Ensure you copy the entire hash string starting from `$pdf$` without missing any characters or adding extra spaces.




<img width="1366" height="768" alt="4_copy the hash value" src="https://github.com/user-attachments/assets/1968f107-e9da-4dbc-8f69-22eae869cc76" />
















### 5. Open the NetworkWalks Password Cracker
* Open a new browser tab and navigate to the <https://networkwalks.com/password-cracker/>



<img width="1366" height="768" alt="5_open networkwalks password cracker" src="https://github.com/user-attachments/assets/375a98d9-87ae-43fd-adc2-7efaf11e7e5b" />














### 6. Paste the Hash & Start the Dictionary Attack
* Paste the copied `$pdf$` hash string into the **PDF HASH (`$pdf$...`)** input field.
* Verify the active wordlist (built-in list or custom `.txt` wordlist) and click **START CRACKING**.
* The tool iterates through candidate passwords in the dictionary until a cryptographic match is found.




<img width="1366" height="768" alt="6_paste hash value in password cracker and start attack" src="https://github.com/user-attachments/assets/516b50c5-761d-44bd-ab5d-f02e99e0832b" />



<img width="1366" height="768" alt="7_cracking in progress" src="https://github.com/user-attachments/assets/b5793c8f-9219-4bca-b8d0-eb0ebcf02ed4" />






### 7. Review the Cracked Password Output
* Wait for the dictionary attack to finish processing.
* Once matched, the tool displays **PASSWORD CRACKED SUCCESSFULLY** along with the recovered plaintext password (`password1`).


<img width="1365" height="753" alt="8_hash value cracked sucessfully" src="https://github.com/user-attachments/assets/c7254833-64de-46f7-8742-b7a006193a83" />







### 8. Open the Locked PDF & Enter the Password
* Locate `My Locked PDF1.pdf` on your computer and double-click to open it in your PDF reader.
* Enter the recovered password (`password1`) into the document password prompt and click **OK**.


<img width="1366" height="768" alt="9_open pdf1 file" src="https://github.com/user-attachments/assets/d4af2bcb-961e-4c4c-b59f-68358a5d0efe" />


<img width="1366" height="767" alt="10_enter password1" src="https://github.com/user-attachments/assets/376185fb-787b-4edc-a9ae-e0c9da13171f" />






### 9. Verify Document Access & Complete the Lab
* Confirm that the encrypted PDF unlocks and displays the congratulatory flag message (`You have captured your 1st flag.`).








<img width="1366" height="768" alt="11_pdf1 file open sucessfully" src="https://github.com/user-attachments/assets/c87318a4-0477-48e2-84b0-65b9bbd120ec" />
















## 📂 Repository Structure

```text
Password-Cracking-With-NetworkWalks-Tools/
├── README.md                                                  # Project documentation, Mermaid architecture & step-by-step walkthrough
├── target/
│   └── My Locked PDF1.pdf                                     # Encrypted PDF file audited in the authorized lab
└── screenshots/
    ├── task-01-download-target-pdf/
    │   └── 01_download_encrypted_pdf1_file.png                # Downloading My Locked PDF1.pdf from NetworkWalks lab page
    ├── task-02-open-hash-calculator/
    │   └── 02_open_networkwalks_hash_calculator.png           # Opening NetworkWalks Hash Calculator in web browser
    ├── task-03-upload-locked-pdf/
    │   └── 03_upload_pdf1_file_to_hash_calculator.png         # Uploading My Locked PDF1.pdf for local client-side parsing
    ├── task-04-copy-extracted-hash/
    │   └── 04_copy_the_hash_value.png                         # Copying the complete extracted pdf cryptographic hash
    ├── task-05-open-password-cracker/
    │   └── 05_open_networkwalks_password_cracker.png          # Opening NetworkWalks Password Cracker dictionary tool
    ├── task-06-execute-dictionary-attack/
    │   ├── 06_paste_hash_value_and_start_attack.png           # Pasting pdf hash and clicking START CRACKING
    │   └── 07_cracking_in_progress.png                        # Dictionary attack iterating through candidate words
    ├── task-07-review-cracked-password/
    │   └── 08_hash_value_cracked_successfully.png             # Plaintext password recovered (password1)
    ├── task-08-unlock-encrypted-pdf/
    │   ├── 09_open_pdf1_file.png                              # Opening My Locked PDF1.pdf in PDF reader
    │   └── 10_enter_password1.png                             # Entering recovered password (password1) into prompt
    └── task-09-verify-access-and-flag/
        └── 11_pdf1_file_opened_successfully.png               # Document unlocked and 1st flag captured
```







---

## 🧠 Key Takeaways & Defensive Mitigations
* **Encryption vs. Hashing:** Encryption is a two-way reversible function requiring a key to decrypt data, whereas hashing is a one-way mathematical function that transforms plaintext into a unique message digest.
* **Speed of Dictionary Attacks:** Common passwords such as `123456`, `password`, or `password1` are cracked almost instantaneously because they appear at the top of standard password dictionaries.
* **Enforce High Password Complexity:** An 8-character lowercase-only password can be cracked in minutes, whereas a 12+ character password mixing uppercase, lowercase, numbers, and symbols significantly increases cracking resistance.
* **Credential Hygiene & Reuse Prevention:** With billions of leaked credentials circulating from historical data breaches, organizations and users must avoid password reuse and implement Multi-Factor Authentication (MFA) wherever supported.

---

## 🔐 Security & Ethical Use
This laboratory and repository are intended strictly for educational and authorized research purposes only. All password auditing activities were conducted within the authorized <https://networkwalks.com> lab scope. Unauthorized cracking or exploitation of external files and systems is illegal.

## 🔗 Tools & Resources
* **Primary Environment:** Windows 10 PRO | <https:networkwalks.com> Week 3 | Project Module 2)
* **Browser-Based Utilities:** <https://networkwalks.com/hash-calculator/> | <https://networkwalks.com/password-cracker/>
* **Official Documentation:** <https://networkwalks.com> 

## 👤 Author
**Anderson Edaiyo Uzezi**  
Cybersecurity Professional B084  
LinkedIn: https://www.linkedin.com/in/anderson-edaiyo-bab74117b





## 📊 Project Information Matrix

> **Note:**  
> This repository contains the complete documentation, environment blueprints, and live verification logs for my Week 03 specialized laboratory deployment focusing on browser-based cryptographic hash extraction, dictionary-driven password auditing, and credential recovery.

| 🗂️ Project Parameter | ⚙️ Live Deployment Data |
| :--- | :--- |
| **Program Track** | Cybersecurity with Ethical Hacking |
| **Academy Module** | Networkwalks Academy Portfolio Matrix |
| **Timeline Horizon** | Week 03 Engineering Core |
| **Project Identity** | Password Cracking with NetworkWalks Tools |
| **Target Task ID** | TASK W3-PM2 |
| **Code Repository** | Public Deployment Hub via GitHub |


