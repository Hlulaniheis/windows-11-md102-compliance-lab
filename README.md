# Windows 11 MD-102 Compliance Lab

## 📌 Project Overview

This project demonstrates enterprise device compliance management using **Microsoft Intune** and **Microsoft Entra ID Conditional Access**. A Windows 11 VM was enrolled in Intune, a compliance policy was applied requiring BitLocker and Defender, and a Conditional Access policy was created to enforce compliant device access.

## 🎯 Objectives

- Enroll a Windows 11 device in Microsoft Intune
- Create and apply a Windows 10/11 compliance policy
- Enforce BitLocker encryption and Defender protection
- Configure Conditional Access to require compliant devices
- Demonstrate device compliance status

## 🏗️ Architecture

Windows 11 VM → Entra ID Join → Intune Enrollment → Compliance Policy → Conditional Access

## 🛠️ Technologies Used

- Windows 11 Pro
- Microsoft Entra ID
- Microsoft Intune
- BitLocker
- Conditional Access

## 📸 Proof of Compliance

![Device Compliant](screenshots/23-device-compliant-final.png)

## 📋 Step-by-Step Process

### 1. Device Enrollment
- Joined Windows 11 VM to Entra ID
- Enrolled device in Intune via MDM user scope

### 2. Compliance Policy
- Created MD102-Lab-Compliance policy
- Requirements: BitLocker, OS version, Defender

### 3. BitLocker Encryption
- Enabled BitLocker on system drive
- Used new encryption mode (XTS-AES)

### 4. Conditional Access
- Created Require-Compliant-Devices policy
- Applies to all cloud apps
- Requires compliant and hybrid joined devices

## 🔧 Challenges & Solutions

| Challenge | Solution |
|-----------|----------|
| MDM URL missing | Restored default MDM URLs in Entra ID |
| Device not enrolling | Re-joined Entra ID and re-added work account |
| BitLocker blocked by ISO | Removed DVD drive ISO |
| Device noncompliant | Enabled BitLocker, synced, restarted |

## 📂 Repository Structure

windows-11-md102-compliance-lab/
├── README.md
├── screenshots/
│ ├── 01-create-policy-start.png
│ ├── 02-policy-basics.png
│ ├── 03-device-health.png
│ ├── 04-device-properties.png
│ ├── 05-defender-settings.png
│ ├── 06-policy-assignments.png
│ ├── 07-review-create.png
│ ├── 08-actions-noncompliance.png
│ ├── 09-bitlocker-recovery-key.png
│ ├── 10-bitlocker-encrypt-used-space.png
│ ├── 11-bitlocker-new-encryption-mode.png
│ ├── 12-bitlocker-system-check.png
│ ├── 13-bitlocker-encrypting.png
│ ├── 14-compliance-policy-status.png
│ ├── 15-compliance-policy-list.png
│ ├── 16-compliance-settings-summary.png
│ ├── 17-entra-id-devices.png
│ ├── 18-access-work-school.png
│ ├── 19-mdm-mobility-settings.png
│ ├── 20-mdm-url-populated.png
│ ├── 21-device-noncompliant.png
│ ├── 22-device-compliant.png
│ ├── 23-device-compliant-final.png
│ ├── 24-conditional-access-policies.png
│ ├── 25-conditional-access-policy-details.png
│ └── 26-device-list-compliant.png

👨‍💻 Author
Hlulani Chavalala — (https://github.com/Hlulaniheis)

📅 Date
July 2026
