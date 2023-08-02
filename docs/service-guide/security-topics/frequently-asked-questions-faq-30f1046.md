<!-- loio30f1046bdff042b2b9134b9fd9f306b3 -->

# Frequently Asked Questions \(FAQ\)

You can find a collection of frequently asked questions and provided solutions.



1.  **How many keys can I've?**

    -   Currently, we support only one key that is the default subaccount key, which is generated by DCKMS during your DCKMS tenant onboarding process.


2.  **Is it possible to rotate the keys? If yes, shall I access the data encrypted with the older key?**

    -   No, the default key rotation is internally managed by the credential store.


3.  **Can I've a default key? If yes, can I switch to my own key if I no longer want the default key?**
    -   There's no support for bringing your own key as a default key.


4.  **Can I enable, disable, and re-enable my key?**

    -    Yes, but the content won't be accessible when the key is disabled.


5.  **What will happen to my encrypted content if I disable the key?**

    -   Content remains encrypted. Since the key is disabled, you can't access the content.


6.  **Can I've my own key to encrypt the content I upload to the SAP Document Management Service repository?**

    -   No, actual encryption keys are internally managed. The default subaccount key from DCKMS is used to encrypt or decrypt the intermediate KEY. This is necessary to encrypt or decrypt the data-encryption keys \(DEKs\) which is used to encrypt or decrypt the content.


7.  **Is it possible to encrypt the content with a symmetric key?**

    -   The default subaccount key automatically generated by the system is symmetric however this isn't the actual data encryption key and this is used to manage the intermediate key encryption key.


8.  **What do you suggest for a key - should I choose a symmetric or an asymmetric key? What is the difference?**

    -   Currently, DCKMS tenant supports only one key that is the default subaccount key automatically generated by the system. This key is symmetric and uses AES encryption.


9.  **Can I use more than one key to encrypt my content?**

    -   No


