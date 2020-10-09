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
- **Security.Encrypt(Key,Plain_Data)** return a **Encryyption_Model** result.
- Parameters : 
- **Key** is the private key for encryption operation.
- **Key** should be in string type.
- **Plain_Data** is the data that you want to encrypt.
- **Plain_Data** (At this time) Should be a string type.
