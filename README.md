# EncryptionTools
* **对称加密 &amp; 解密**
  * DES(ECB)加密
    $ echo -n hello | openssl enc -des-ecb -K 616263 -nosalt | base64
  * DES(CBC)加密
    $ echo -n hello | openssl enc -des-cbc -iv 0102030405060708 -K 616263 -nosalt | base64
  * AES(ECB)加密
    $ echo -n hello | openssl enc -aes-128-ecb -K 616263 -nosalt | base64
  * AES(CBC)加密
    $ echo -n hello | openssl enc -aes-128-cbc -iv 0102030405060708 -K 616263 -nosalt | base64
  * DES(ECB)解密
    $ echo -n HQr0Oij2kbo= | base64 -D | openssl enc -des-ecb -K 616263 -nosalt -d
  * DES(CBC)解密
    $ echo -n alvrvb3Gz88= | base64 -D | openssl enc -des-cbc -iv 0102030405060708 -K 616263 -nosalt -d
  * AES(ECB)解密
    $ echo -n d1QG4T2tivoi0Kiu3NEmZQ== | base64 -D | openssl enc -aes-128-ecb -K 616263 -nosalt -d
  * AES(CBC)解密
    $ echo -n u3W/N816uzFpcg6pZ+kbdg== | base64 -D | openssl enc -aes-128-cbc -iv 0102030405060708 -K 616263 -nosalt -d

>提示：
 1、 加密过程是先加密，再base64编码
 2、 解密过程是先base64解码，再解密
