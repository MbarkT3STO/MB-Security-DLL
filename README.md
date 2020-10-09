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
- **Security.Encrypt( Key , Plain_Data )** return a **Encryyption_Model** result.
-
- **Parameters** : 
-
- **Key** is the private key for encryption operation.
- **Key** should be in string type.
- **Plain_Data** is the data that you want to encrypt.
- **Plain_Data** (At this time) Should be a string type.

```
string Original_Data = "My name is MBARK";
Encryption_Model em = Security.Encrypt("MyPrvKey", Original_Data);
```
- Now we **Encrypt** **Original_Data** value, and to get the encrypted data :
```
em.Encrypted_Text
```

- If you want to get the **Key** used after the encryption operation :
```
em.Key
```

- **Decryption**
- To decrypt data use **Decrypt** static function inside **Security** class.
- **Security.Decrypt( Key , Encrypted_Data )** return a **Decryption_Model** result.
-
- **Parameters** : 
-
- **Key** is the private key for decryption operation.
- **Key** should be in string type.
- **Encrypted_Data** is the data that you want to decrypt (should be encrypted already).
- **Encrypted_Data** (At this time) Should be in string type.

```
string Encrypted_Data = "mUVKmyTM/vTYNs35G1LkB7hrKzzno19h";
Decryption_Model dm = Security.Decrypt("MyPrvKey", Encrypted_Data);
```

- **Other Example for Decryption**
```
string Original_Data = "My name is MBARK";

Encryption_Model em = Security.Encrypt("MyPrvKey", Original_Data);

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

- **Encryption_Model** and **Decryption_Model** two classes used as a data **models**
