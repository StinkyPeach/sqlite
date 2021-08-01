# GORM Sqlite Cipher Driver

## Description

Go SQLite3 driver for [GORM](https://gorm.io/) by encrypting the SQLite3 database with AES-256 conforming to the built-in database / SQL interface

## USAGE

```go
import (
  "fmt"
  sqlite "github.com/StinkyPeach/sqlite"
  "gorm.io/gorm"
)

key := "your's key"
dbName := "test.db"
DSN := dbName + fmt.Sprintf("?_pragma_key=%s&_pragma_cipher_page_size=4096", key)
db, err := gorm.Open(sqlite.Open(DSN), &gorm.Config{})
```

Checkout [https://gorm.io](https://gorm.io) for details.

<details>
<summary>Acknowledgement</summary>

- [go-gorm/sqlite](https://github.com/go-gorm/sqlite)  
- [sqlcipher/sqlcipher](https://github.com/sqlcipher/sqlcipher)  

</details>
