# EncryptedMessengerApplication
This project focuses the sending-receiving message (over TCP Socket) with high security. The RSA and AES were used in this application for providing high security.  The project sceneario;  

1.) The public and private keys which are 1024 bits and they are generated for RSA by KeyPairGenerator java class.  

2.) After this key generating process, the public key is sent to clients over TCP Socket connection.  

3.) Client gets the public key of Server now. Client generate asymmetric key (symmetric key will be used for AES encrytion) which are encrypted by RSA public key and this encrypted message will be sent to Server.  

4.) Server is got the symmetric key now.  

5.) Server decrypts this message with its private key and Server reaches the symmetric key.  

6.) Now, Server can encrypt the messages by using this AES symmetric key and after that encryption, it sends this message over TCP Socket to Client.  

7.) Client decrypts this message (from Server) with its AES symmetric key.  

And this loop can continue until TCP Socket is terminated by Server or Client user so  very high secure messanger application can be implemented on Java by this way. The 3rd party users can not reach your message, no way! Thanks to RSA and AES so much!!! :-)
