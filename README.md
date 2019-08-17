### jpad
---
http://jpad.io/

```java
// JPADCore/src/database/databasefunctions/DatabaseReader.java
package database.databasefunctions;

import java.io.File;
import java.net.URL;

import standaloneutils.database.hdf.MyHDFReader;

public abstract class DatabaseReader {
  protected String databaseFolderPath, databaseFileName;
  
  protected URL databaseFolder;
  protected MyHDFReader database;
  
  public DatabaseReader(String databaseFolderPath, String databaseFileName) {
    this.databaseFolderPath = databaseFolderPath;
    this.databaseFileName = databaseFileName;
    
    if (!databasefolderPath.endsWith(File.separator)) databaseFolderPath = databaseFolderPath + File.separator;
    
    String databaseFileNameWithPath = databasefolderPath + databaseFileName;
    
    database = new MyHDFReader(databaseFileNameWithPath);
  }
}

```

```
```

```
```


