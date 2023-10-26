# 2023 Date Note 연습
[2023](2023/2023.md)

# Folder
```dataview
TABLE file.mday as 수정일, file.cday as 생성일, file.size as "파일 크기"
WHERE
	length(split(regexreplace(replace(file.folder, this.file.folder, ""), "^/", ""),  "/")) = 1
	AND startswith(file.name, "0 ")
	AND startswith(file.folder, this.file.folder)
	AND file.name != this.file.name
SORT file.name ASC
```

# MD File
```dataview
TABLE file.mday as 수정일, file.cday as 생성일, file.size as "파일 크기"
WHERE
	file.folder = this.file.folder
	AND file.name != this.file.name
SORT file.mday DESC
```
