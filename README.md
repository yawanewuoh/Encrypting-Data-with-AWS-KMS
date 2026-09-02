<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Encrypt Data with AWS KMS

**Project Link:** [View Project](http://nextwork.ai/projects/aws-security-kms)

**Author:** Jude Anewuoh  
**Email:** judeanewuoh@gmail.com

---

![Image](http://nextwork.ai/positive_beige_noble_river_dolphin/uploads/aws-security-kms_w0x1y2z3)

---

## Introducing Today's Project!

In this project, I did the following: 
1. Created encryption keys with AWS KMS (Key Management Service).
2. Encrypted a DynamoDB database with a KMS key.
3. Observed how AWS stops unauthorized access to data.
4. Granted a user encryption access.

### Tools and concepts

Services I used include AWS Key Management System (KMS). Key concepts I learnt include encryption, which ensures data is stored in a secure format known as ciphertext. I also learn't about access controls and encryption solves different probelms. 

Access controls blocks access to a resource or data whiles encryption ensures data is protected and confidential to only authorised users.

### Project reflection

This project took me approximately 40 minutes. It opened my eye on data security and how AWS KMS is used in the encryption of data.

I chose to do this project today because I wanted to enhance my cloud security skills. 

---

## Encryption and KMS

Encryption is the process of converting data into a secure format called ciphertext. Companies and developers do this to meet compliance requirements for data security. Encryption keys are keys for encrypting the data.

AWS KMS is a secure vault for your encryption keys. Key management systems are important because they manage your encryption keys, that is, what data it encrypts and who has access to it.

Encryption keys are broadly categorized as symmetric or asymmetric. I set up a symmetric key because I wanted to use the same key to encrypt and decrypt data.

![Image](http://nextwork.ai/positive_beige_noble_river_dolphin/uploads/aws-security-kms_a2b3c4d5)

---

## Encrypting Data

My encryption key will safeguard data in DynamoDB, which is a no-sql database I created.

The different encryption options in DynamoDB include AWS owned key, AWS managed key and Customer managed key. Their differences are based on how they are managed. I selected Customer managed key.

![Image](http://nextwork.ai/positive_beige_noble_river_dolphin/uploads/aws-security-kms_q8r9s0t1)

---

## Data Visibility

Rather than controlling who has access to the key, KMS manages user permissions by assigment. 

Despite encrypting my DynamoDB table, I could still see the table's items because of a feature called transparent data encryption. DynamoDB uses transparent data encryption, which ensures data at rest that is encrypted, is decrypted before it gets to authorized users or applications.

![Image](http://nextwork.ai/positive_beige_noble_river_dolphin/uploads/aws-security-kms_c0d1e2f3)

---

## Denying Access

I configured a new IAM user to have access to DynamoDB data. The permission policies I granted this user are AmazonDynamoDBFullAcess.

After accessing the DynamoDB table as the test user, I encountered an access denial error because I (test user) wasn't authorized to this that data. This confirmed the encryption was working as expected.

![Image](http://nextwork.ai/positive_beige_noble_river_dolphin/uploads/aws-security-kms_w0x1y2z3)

---

## EXTRA: Granting Access

To let my test user use the encryption key, I gave a key use access. My key's policy was updated to two users, adding the test user as new entrant.

Using the test user, I retried accessing the DynamoDB table and observed that the access denial error was no longer present, confirming that the test user is now authorised to view the encrypted data.

Encryption secures data instead of controlling access. I could combine encryption with access controls to protect sensitive data.

![Image](http://nextwork.ai/positive_beige_noble_river_dolphin/uploads/aws-security-kms_feffb2fb8)

---

---
