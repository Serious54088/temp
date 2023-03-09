CSV文件没有官方的标准，但一般项目都会遵守 **RFC 4180** 标准。这是一个非官方的标准，内容如下：

> 1.  Each record is located on a separate line, delimited by a line break (CRLF).
>     
> 2.  The last record in the file may or may not have an ending line break.
>     
> 3.  There maybe an optional header line appearing as the first line of the file with the same format as normal record lines. This header will contain names corresponding to the fields in the file and should contain the same number of fields as the records in the rest of the file (the presence or absence of the header line should be indicated via the optional "header" parameter of this MIME type).
>     
> 4.  Within the header and each record, there may be one or more fields, separated by commas. Each line should contain the same number of fields throughout the file. Spaces are considered part of a field and should not be ignored. The last field in the record must not be followed by a comma.
>     
> 5.  Each field may or may not be enclosed in double quotes (however some programs, such as Microsoft Excel, do not use double quotes at all). If fields are not enclosed with double quotes, then double quotes may not appear inside the fields.
>     
> 6.  Fields containing line breaks (CRLF), double quotes, and commas should be enclosed in double-quotes.
>     
> 7.  If double-quotes are used to enclose fields, then a double-quote appearing inside a field must be escaped by preceding it with another double quote.

翻译一下：

1、每条记录位于单独的行上，由换行符 (CRLF) 分隔。

2、文件中的最后一条记录可能有也可能没有结束换行符。

3、可能有一个可选的标题行出现在文件的第一行，格式与普通记录行相同。此标题将包含与文件中的字段对应的名称，并且应包含与文件其余部分中的记录相同数量的字段（标题行的存在或不存在应通过此 MIME 类型的可选“标头”参数指示）。

4、在标题和每条记录中，可能有一个或多个字段，以逗号分隔。在整个文件中，每行应包含相同数量的字段。空格被视为字段的一部分，不应忽略。记录中的最后一个字段后面不能有逗号。

5、每个字段可以用双引号括起来，也可以不用双引号（但是某些程序，例如 Microsoft Excel，根本不使用双引号）。如果字段没有用双引号括起来，那么双引号可能不会出现在字段内。

6、包含换行符 (CRLF)、双引号和逗号的字段应该用双引号括起来。

7、如果使用双引号将字段括起来，则出现在字段中的双引号必须在其前面加上另一个双引号。