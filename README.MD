# 1.1 ExportHelper 是什么？

> **ExportHelper.js 是一款便利的前端文件导出 lib 库**

# 1.2 用法

```javascript
//浏览器平台
const ExportHelper = window.ExportHelper;
// commonjs
const ExportHelper = require("xxx/export-helper.js");
// es6 Module
import * as ExporHelper from "xxx/export-helper.js";
```

# 1.3 API

## ExportHelper.download(filename, text, mime);

## 参数：

- **filename**
  > - **String **【必填】。
  >   需要导出或者下载的文件名。
- **text**
  > - **String **【必填】。
      需要写入文件的内容。
- **mime**
  > - **String **【选填】。
      需要写入文件的MIME类型 默认为：text/csv。

## 返回值: 无。

## ExportHelper.CSV(data,options);

> 对存储到 csv 的数据进行编码和解码的对象。采用了第三方库具体文档请移步 github：[csv.js 文档](https://github.com/knrz/CSV.js/tree/3.6.4)

## ExportHelper.exportCsv(data,options,filename);

## 参数：

- **data**
  > - **Array**【必填】。
  >   需要进行编码的数据，同 csv.js 的参数作用一致，请具体参考 csv.js 文档。
- **options**
  > - **object **【可选】。
      编码过程中的配置选项，默认为 {}。同csv.js的参数作用一致，请具体参考csv.js文档。
- **filename**
  > - **String **【必填】。
  >   需要导出或者下载的文件名，默认为 download.csv 。

## 返回值: 无。

## ExportHelper.parseCsv(text,options)；

- **text**
  > - **String**【必填】。
      需要进行解码的字符串。同csv.js的参数作用一致，请具体参考csv.js文档
- **options**
  > - **object **【可选】。
      编码过程中的配置选项，默认为 {}。同csv.js的参数作用一致，请具体参考csv.js文档

## 返回值:

> **Array: 返回解码后包含这些数据的数组。**
