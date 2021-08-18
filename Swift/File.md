## File

### 列出制定目录文件列表
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

### 列出指定目录文件列表，是否包含子目录，按文件名排序
##### List files in path order include/exclude sub folders

```
import Foundation

let manger = FileManager.default
let url = URL(string: "/Users/dvpr/Developer/workspace/git/dvpr.github.io")

// include sub folders
let enumerator = manger.enumerator(at: url!, includingPropertiesForKeys: nil, options: .skipsHiddenFiles, errorHandler: nil)

// order by name
var enumeratorArray: [URL] = []
while let element = enumerator?.nextObject() as? URL { enumeratorArray.append(element) }
let enumeratorSorted = enumeratorArray.sorted(by: {(s1, s2) in
    return s1.path < s2.path
})

for item in enumeratorSorted {
    print(item)
}

// exclude sub folders
let items: [URL] = try! manger.contentsOfDirectory(at: url!, includingPropertiesForKeys: nil, options: .skipsHiddenFiles)

// order by name
let itemsSorted = items.sorted(by: {(s1, s2) in
    return s1.path < s2.path
})

for item in itemsSorted {
    print(item)
}
```

##### 读取文件内容
##### Read content of file

```
import Foundation

let manager = FileManager.default

let data = manager.contents(atPath: "/path/to/your/file")
let string = String(data: data!, encoding: String.Encoding.utf8)
print(string)
```