# DRDO CTF 2017 : Crypto-8

**Category:** Crypto

**Level:** Hard

**Points:** 200

**Solves:** 149

**Description:**

Early CCS or CCS Injection is a vulnerability which was discovered in OpenSSL in 2014. This vulnerability allows the server to accept the ChangeCipherSpec message (This message is used to inform that all message following this message are going to be encrypted) of TLS protocol earlier(before ClientKeyExchange message) than expected. 
Due to its early acceptance of CCS message **keys are not exchanged but encryption starts** and client sends an encrypted ClientKeyExchange message. This encrypted ClientKeyExchange message is similar to plain ClientKeyExchange message but it is encrypted due to early acceptance of CCS message. 
ClientKeyExchnage message contains an **encrypted PreMasterSecret which is encrypted using RSA-2048 public key**. Decrypt the contents to attached file of capture the FLAG.

## Additional Information

* TLS Version: 1.0
* Server Private key: cyber\_challenge.key (This file was not uploaded.)
* PCAP: DecryptMe.pcapng
* Key\_Block.JPG, Master\_Secret.JPG, PRF\_Phash.JPG and rfc2246.txt will help you to understand the protocol and decrypt the content.


## Help
* In wireshark to see the captured packets as TLS message for port 1024:

Go to Wireshark->Analyze tab --> Decode As --> type port 1024 and select SSL protocol. Now it will show packets as SSL/TLS Messages from the port 1024

## Online Resources

* Internet Search: “CCS Injection”, CVE-2014-0224
* TLS 1.0 RFC: https://www.ietf.org/rfc/rfc2246.txt

## Attachments

[DecryptMe.pcapng](DecryptMe.pcapng)

(Following file has the flag itself. It was uploaded by mistake. A similar challenge Crypto-9 was added later.)

[Problem\_8\_Hard.txt](Problem\_8\_Hard.txt)

[rfc2246.txt](rfc2246.txt)

![Key\_Block.JPG](Key\_Block.JPG)

![Master\_Secret.JPG](Master\_Secret.JPG)

![PRF\_PHash.JPG](PRF\_PHash.JPG)


## Write-up  (For correct challenge, please refer to Crypto-9)

Flag of this challenge was mistakenly uploaded in attachment `Problem\_8\_Hard.txt`. 

Flag is : `DRDO@60_{G8F05E}_FLAG!`

For correct version of challenge, plese refer to Crypto-9 challenge
