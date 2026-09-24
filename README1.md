# NETWORKWALKS-B083-WK3-PM1_2-CYBERSECURITY-PASSWORD-CRACKING
## Password-Protected PDF Security Assessment

This repository documents my Week 3 practical project completed as part of my Cybersecurity & Ethical Hacking Internship at Networkwalks.

The practical focused on understanding how password-protected PDF documents can be assessed through offline password recovery techniques. The exercise covered extracting the authentication data required by a password-recovery tool and using controlled password-guessing techniques to recover passwords for authorized laboratory files.

**Educational use only:** All password-recovery activities documented in this repository were performed as part of authorized cybersecurity training. The techniques must only be used against files, systems, and accounts that you own or have explicit permission to assess.

# Overview

Password-protected documents are designed to prevent unauthorized access. From a cybersecurity perspective, however, password protection can be assessed by examining how difficult the password is to recover through offline guessing.

**This practical covered two workflows:**

- PDF authentication-data extraction followed by password recovery with John the Ripper

- Hash calculation followed by password recovery using the Networkwalks training platform

**The exercise demonstrated the relationship between:**

- Password protection

- Hashes and password-derived authentication data

- Wordlists and password-guessing techniques

- Password recovery tools

- Password strength

- Secure handling of protected documents

 
# Learning Objectives

**The objectives of this practical were to:**

- Understand the role of password protection in PDF documents.

- Understand the difference between a password and the authentication data used to verify it.

- Extract the data required for an authorized password-recovery assessment.

- Use John the Ripper to perform an offline password-recovery exercise.

- Understand how password lists and guessing strategies affect recovery.

- Use a controlled cybersecurity training platform to perform a second password-recovery workflow.

- Verify recovered passwords by successfully opening the protected documents.

- Document cybersecurity activities in a reproducible and professional manner.

- Understand why strong, unique passwords are important for protecting sensitive information.

# About Johnny:
John the Ripper is an open-source password security auditing and password-recovery tool with support for many password, hash, cipher, archive, and document formats, including password-protected PDF files in its Jumbo version. \
For John the Ripper, the official Openwall documentation provides information on installation, supported formats, cracking modes, options, and usage examples.

John the Ripper supports multiple password-recovery modes, including wordlist-based approaches and other configurable strategies. \
Its official documentation describes the use of wordlists and password-mangling rules for authorized password auditing.

# Practical Activities
## Task 1 — PDF Authentication Data Extraction and Password Recovery
### Step 1: Extract the PDF Authentication Data

For the first part of the exercise, the password-protected PDF files were processed using the **OnlineHashCrack PDF Hash Extractor**.

The extracted data was saved to a text file for use during the password-recovery stage.

 ***Security consideration:*** Uploading a real or confidential document to a third-party online service can expose its contents or metadata. 
 
 For real-world security assessments, use locally controlled tools and synthetic/lab data unless an external service has been explicitly approved.

### Step 2: Password Recovery with John the Ripper

The extracted data was then provided to John the Ripper for the password-recovery exercise.

The recovered password was then used to open the corresponding protected PDF.

After entering the recovered password, the PDF opened successfully.

## Result

*PDF 3:* Successfully opened after authorized password recovery.

The same assessment methodology was applied to the second protected PDF.

## Result

*PDF 2:* Successfully opened after authorized password recovery.

## Task 2 — Networkwalks Hash Calculator and Password Cracker
### Step 1: Generate the Hash

For the second workflow, the protected PDF was processed using the Networkwalks Hash Calculator.

The resulting value was copied for use in the password-recovery stage.

### Step 2: Password Recovery

The generated value was entered into the Networkwalks Password Cracker provided as part of the training exercise.

The recovery process was monitored until completion.

Once processing was complete, the recovered password was displayed.

The recovered password was then used to open the protected PDF.

## Result

*PDF 1:* Successfully opened after authorized password recovery.

## Results Summary
File Authentication Data Extracted Recovery Method Result
PDF 3 Yes John the Ripper Successfully recovered
PDF 2 Yes John the Ripper Successfully recovered
PDF 1 Yes Networkwalks Password Cracker Successfully recovered

The practical demonstrated that password-protected documents can be vulnerable to offline password-guessing when the underlying password is sufficiently predictable or weak.

The exercise also demonstrated an important security principle: the difficulty of recovering a password depends heavily on the password itself, the protection mechanism, and the resources available to an attacker.

| Tools Used | Tool Purpose |
|------------|--------------|
| OnlineHashCrack PDF Hash Extractor | Extract authentication data from the authorized PDF files |
| John the Ripper | Perform an offline password-recovery assessment |
| Networkwalks Hash Calculator | Generate the value required for the training exercise |
| Networkwalks Password Cracker | Perform the second controlled password-recovery exercise |

## Key Cybersecurity Concepts

- Password Hashing and Verification

- Password systems generally do not need to store passwords in plaintext. Instead, they can store password-derived values that allow the system to verify a password without directly storing the original password.

- During an offline password-recovery assessment, a tool generates candidate passwords and checks whether they produce the expected authentication value.

- Therefore, it is more accurate to describe the process as password guessing/recovery rather than simply "converting a hash back into a password."

## Offline Password Recovery

- Offline recovery differs from repeatedly attempting to log in to an online service.

- In an offline scenario, an assessor has access to the relevant authentication data and can test candidate passwords locally. This means that traditional online protections such as login throttling or account lockout may not apply.

- John the Ripper provides several password-recovery modes and can use wordlists and transformation rules to generate password candidates.

## Password Strength

- A password that is short, predictable, reused, or based on common words is generally easier to guess than a long and unique password.

## Factors affecting password-recovery difficulty include:

- Password length

- Password unpredictability

- Character selection

- Use of common words or patterns

- Password reuse

- Attack strategy

- Wordlist quality

- Available computing resources

- Strength of the underlying cryptographic protection

# Lessons Learned

## This practical helped me understand the following cybersecurity concepts:

### Password Protection

I learned how password protection can be assessed from a security perspective and why password strength is an important component of document security.

### Authentication Data

I learned that password-recovery tools generally work with password-derived authentication data rather than simply "decrypting" a password hash.

### Offline Password Recovery

I learned how password-recovery tools can test large numbers of candidate passwords against locally available authentication data.

### Wordlists and Password Patterns

I learned that the effectiveness of a password-recovery exercise depends significantly on the candidate-password strategy and the characteristics of the password being assessed.

### Security Documentation

**I learned the importance of documenting:**

The objective

Tools used

Methodology

Evidence

Results

Security considerations

# Lessons learned

Professional cybersecurity work should be reproducible while avoiding unnecessary disclosure of sensitive information.

## Security and Ethical Use

This repository is intended strictly for authorized cybersecurity education, research, and training.

**Password-recovery techniques must only be used against:**

- Files that you own

- Laboratory files provided for training

- Systems where you have explicit authorization

- Data covered by an approved security assessment

- Do not use these techniques to access another person's files, accounts, systems, or data without permission.

### Handling Sensitive Documents

Real documents should not be uploaded to third-party hash-extraction or password-recovery services unless their use has been explicitly authorized.

**For professional assessments, prefer:**

- Synthetic test files

- Dedicated laboratory environments

- Locally controlled tools

- Approved organizational infrastructure

- Properly documented authorization

### Limitations

The results of this practical should not be interpreted as evidence that every password-protected PDF can be recovered.

### Password recovery can fail when:

- The password is sufficiently long and unpredictable.

- The candidate password is not present in the selected wordlist.

- The attack strategy does not match the password's structure.

- The document uses a stronger protection configuration.

- The available computational resources are insufficient.

- The required PDF format is not supported by the selected tool/version.

- John the Ripper's documentation also notes that support for particular document formats can depend on the version/build being used, with PDF processing commonly involving the appropriate *2john utility in Jumbo builds.

# References

John the Ripper — Official Website: Openwall John the Ripper

John the Ripper Documentation

John the Ripper Usage Examples

John the Ripper Cracking Modes

Networkwalks Hash Calculator 

Networkwalks Password Cracker

# Author
**Sikhanyiso B. Sibisi**
Cybersecurity Intern - B083

LinkedIn: https://za.linkedin.com/in/sikhanyiso-b-s-a28a0b13a

# Project Information
GitHub | Repository|
-------|-----------|
Program Name| Cybersecurity at Networkwalks |
Project | Cybersecurity - Password Cracking | 
Instructor | Waqas Karim |
Week | 03 | 

# Conclusion

This practical demonstrated the basic workflow involved in an authorized password-security assessment of protected PDF documents.

The exercise showed how authentication data can be extracted from a protected document, supplied to a password-recovery tool, and assessed using controlled password-guessing techniques.

More importantly, the exercise reinforced the defensive lesson behind password cracking: password protection is only as strong as the cryptographic protection and password practices supporting it.

The practical therefore provided experience with both the technical process of password recovery and the security principles required to protect against unauthorized password attacks.

This version also fixes an important technical issue in the original: John the Ripper does not “read the hashed key and convert it to a readable password.” It tests candidate passwords against the extracted authentication data until a candidate is found that satisfies the verification process. That distinction makes the documentation considerably more accurate.
