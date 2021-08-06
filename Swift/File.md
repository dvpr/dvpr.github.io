## File

##### List files in path

```
import Foundation

let manger = FileManager.default
let url = URL(string: "/path/to/your/path")

let enumerator = manger.enumerator(at: url!, includingPropertiesForKeys: nil, options: .skipsHiddenFiles, errorHandler: nil)

while let element = enumerator?.nextObject() as? URL {
    print(element)
}
```

##### Read content of file
```
import Foundation

let manager = FileManager.default

let data = manager.contents(atPath: "/path/to/your/file")
let string = String(data: data!, encoding: String.Encoding.utf8)
print(string)
```