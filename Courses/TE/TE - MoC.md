---
author: Me
theme: "[MapOfContent] TE"
assignment: TE
state: Done
link: 
pin: true
type: course
---
[Go Up](Courses%20-%20MoC.md)
# Expression Technicals

## Nodes
```dataview
TABLE 
	theme AS "subject",
	assignment AS "ass.",
	semester AS "sem."
FROM "Courses/TE"
WHERE type = "full"
SORT file.cday ASC
```

## S3
```dataview
TABLE 
	theme AS "subject",
	type
FROM "Courses/TE"
WHERE semester = "S3"
SORT theme ASC, file.ctime ASC
```

## All
```dataview
TABLE 
	theme AS "subject",
	semester AS "sem."
FROM "Courses/TE"
WHERE type != "full" AND file.name != "TE - MoC"
SORT semester DESC, theme ASC, file.ctime ASC
```