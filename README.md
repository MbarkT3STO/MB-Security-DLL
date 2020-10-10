# MB-Security-DLL
A DLL library for ( .NET ) help you to Encrypt &amp; Decrypt data
# 1st Step (Add reference)
# -----------------------------------------------------------------
- **1 -** Open your .NET project using visual studio.
- **2 -** Go to Solution Explorer
- **3 -** Right click on References
- **4 -** Chose Add Reference
- **5 -** Click on Browse
- **6 -** Select all downloaded DLLs
- **7 -** Click on OK

# 2nd Step (Using)
# -----------------------------------------------------------------
- First thing you should do is inside your **.cs** || **Class** code use the **Name Space** :  

```
using MB_Security;
```

- At this time this Library covering (Encrypt) just **String** data

# Examples
# -----------------------------------------------------------------
- **Encryption**
- To encrypt data use **Encrypt** static function inside **Security** class.
- **Security.Encrypt( Plain_Data , Key )** return a **Encryyption_Model** result.
-
- **Parameters** : 
-
- **Plain_Data** is the data that you want to encrypt.
- **Plain_Data** (At this time) Should be a string type.
- **Key** [ Optional parameter ] is the private || RGB key for encryption operation.
- **Key** should be in string type, and **contains 8 Chars**.
- **Key** If you don't pass it, a Key will **Auto Generated**.
- **IV** [ Optional parameter ] The Initialization vector to use, and **Should be a byte array**.
- **IV** By default IV used is **0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F**

```
string Original_Data = "My name is MBARK";
Encryption_Model em = Security.Encrypt( Original_Data , "MyPrvKey" );
```
- Now we **Encrypt** **Original_Data** value, and to get the encrypted data :
```
em.Encrypted_Text
```

- If you want to get the **Key** used after the encryption operation (Key in encrypted state) :
```
em.Key
```

- **Decryption**
- To decrypt data use **Decrypt** static function inside **Security** class.
- **Security.Decrypt( Encrypted_Data , Key )** return a **Decryption_Model** result.
-
- **Parameters** : 
-
- **Encrypted_Data** is the data that you want to decrypt (should be encrypted already).
- **Encrypted_Data** (At this time) Should be in string type.
- **Key** [ Optional parameter ] is the private || RGB key for decryption operation.
- **Key** should be in string type, **contains 8 Chars**, and **should be the Encrypted key you got after the Encryption operation**.
- **IV** [ Optional parameter ] The Initialization vector to use, and **Should be a byte array**.
- **IV** By default IV used is **0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F**

```
string Encrypted_Data = "mUVKmyTM/vTYNs35G1LkB7hrKzzno19h";
Decryption_Model dm = Security.Decrypt( Encrypted_Data , "MyPrvKey" );
```

- **Other Example for Decryption**
```
string Original_Data = "My name is MBARK";

Encryption_Model em = Security.Encrypt( Original_Data , "MyPrvKey" );

Decryption_Model dm = Security.Decrypt(em.Key, em.Encrypted_Text);

```

- Now we **Decrypt** data, and to get the decrypted data :
```
dm.Decrypted_Text
```

- If you want to get the **Key** used after the decryption operation :
```
dm.Key
```

# Additional info
# -----------------------------------------------------------------

- **Encryption_Model** and **Decryption_Model** two classes used as data **models**
