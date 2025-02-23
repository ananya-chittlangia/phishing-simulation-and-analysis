# Phishing Simulation and Analysis Report

## Disclaimer
This report is strictly for **educational and ethical hacking awareness purposes only**. Unauthorized use of these techniques for malicious purposes is illegal and against ethical cybersecurity practices. Always obtain proper authorization before conducting any penetration testing activities.

---

## Introduction

Phishing attacks are a form of social engineering, where fraudulent messages are sent to a target, pretending to be from a trusted source. The goal is to trick the target into revealing sensitive information like passwords, payment information, etc.

Phishing works like bait in fishing. Attackers send fraudulent messages via email or messaging apps that trick users into entering sensitive data on fake websites designed to look authentic. Once submitted, the attacker gains control over the account.

A phishing attack starts with a fraudulent message, often delivered through email or messaging applications. The target is tricked into opening a malicious link and providing sensitive details on a counterfeit website. These websites closely mimic legitimate ones. Once credentials are submitted, they are transferred to the attacker, who can then exploit the compromised account.

---

## Types of Phishing Attacks

### 1. Email Phishing / Deceptive Phishing
- The most common phishing technique.
- Attackers send mass spam emails pretending to be from a trusted organization.
- Aim: Obtain confidential information like passwords, banking details, and user IDs.

### 2. Spear Phishing
- A targeted attack on a specific individual or organization.
- The attacker gathers information about the victim to craft a convincing phishing email.

### 3. Whaling
- A form of spear phishing targeting high-profile individuals (e.g., CEOs, CFOs).
- Emails create urgency, pressuring executives to make quick decisions.

### 4. Smishing (SMS Phishing)
- Phishing through text messages.
- Users receive SMS with malicious links leading to phishing websites.

### 5. Vishing (Voice Phishing)
- Attackers impersonate trusted entities over phone calls.
- Caller ID spoofing is used to appear authentic.

### 6. Clone Phishing
- Attackers copy legitimate emails, replacing attachments or links with malicious ones.
- The fraudulent emails are sent from an address similar to the original sender.

---

## Tools for Phishing

1. **Gophish**
2. **Speed Phish Framework**
3. **Social-Engineer Toolkit (SET)**
4. **Phishing Frenzy**
5. **ShellPhish**
6. **Hawkeye**
7. **Zphisher** (used in this simulation)

---

## Phase 1: Setup

### Required Tools
- [VirtualBox](https://www.virtualbox.org/)
- [Kali Linux](https://www.kali.org/get-kali/#kali-platforms)
- [Zphisher](https://github.com/htr-tech/zphisher)
- Apache & MariaDB (for hosting phishing pages locally)

### Installation Guide
1. Install VirtualBox and set up Kali Linux.
2. Open the terminal in Kali Linux and clone Zphisher:
   ```sh
   git clone https://github.com/htr-tech/zphisher.git
   cd zphisher
   bash zphisher.sh
   ```
3. Choose the phishing template (e.g., `04` for Microsoft Login page).
4. Copy the generated phishing link and open it in a browser.

#### Screenshots:
![Screenshot 1](Images/1.png)
![Screenshot 2](Images/2.png)

---

## Phase 2: Delivering the Phishing Page

### Steps to Send a Phishing Email
1. Create an email posing as an official source (e.g., Microsoft support).
2. Use **email spoofing** tools to make the email look authentic.
3. Generate an email list using GitHub Crosslinked.
4. Send phishing emails containing the fake login page link.

#### Screenshots:
![Screenshot 3](Images/3.png)
![Screenshot 4](Images/4.png)

---

## Phase 3: Capturing Credentials

### Steps to Extract Credentials
1. Once the victim enters credentials, they are stored in the `auth` directory.
2. Use the command to view stolen credentials:
   ```sh
   cat usernames.dat
   ```

#### Screenshots:
![Screenshot 5](Images/5.png)
![Screenshot 6](Images/6.png)

---

## Phase 4: Implications and Prevention

### What This Demonstrates
- Understanding vulnerabilities in login mechanisms.
- Practical application of phishing techniques in a controlled environment.
- How attackers can exploit weak authentication systems.

### Prevention Strategies
1. **Download from Authorized Sources:** Only install software from official sources.
2. **Maintain Confidentiality:** Do not share personal details through unknown links.
3. **Check Website URLs:** Verify URLs before entering any credentials.
4. **Avoid Responding to Suspicious Emails:** If an email seems questionable, contact the sender through an official channel.
5. **Use Phishing Detection Tools:** Utilize browser security features to block malicious sites.
6. **Avoid Public Wi-Fi:** Public networks increase the risk of cyber threats.
7. **Keep System Updated:** Install security patches to protect against evolving threats.
8. **Enable Firewalls:** Firewalls filter out suspicious data and prevent unauthorized access.

---

## Conclusion

Phishing remains one of the most dangerous cybersecurity threats, exploiting human vulnerabilities rather than technical weaknesses. Cybercriminals continuously evolve their tactics, making phishing attacks more sophisticated and difficult to detect.

By adhering to best security practices such as email verification, secure browsing, and phishing detection tools, individuals and organizations can minimize risks and promote a more secure digital environment.

---

## Important Reference Resources
- [Zphisher GitHub Repository](https://github.com/htr-tech/zphisher)
- [Phishing Awareness Training](https://www.cisa.gov/sites/default/files/publications/Phishing_Guidance.pdf)
- [Burp Suite for Security Testing](https://portswigger.net/burp/documentation/desktop/getting-started/download-and-install)
