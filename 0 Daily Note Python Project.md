# Kanban
[1 Daily Note Python Project Kanban](1%20Daily%20Note%20Python%20Project%20Kanban.md)

# Sub Project
[연도 폴더에 날짜 노트 만드는 프로젝트](연도%20폴더에%20날짜%20노트%20만드는%20프로젝트.md)
[2023](2023/2023.md)

# Note


# Reference
[달력 주차 계산](달력%20주차%20계산.md)
[date 명령어 week-ww-WW](date%20명령어%20week-ww-WW.md)
[각 Date Note에 대한 UI를 생각해서 적어봄](각%20Date%20Note에%20대한%20UI를%20생각해서%20적어봄.md)

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
