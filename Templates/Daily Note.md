---
created: <% tp.file.creation_date() %>
---
tags:: [[+Daily Notes]]

# <% moment().format("dddd, MMMM Do YYYY, h:mm:ss a") %>

<< [[Journal/Daily/<% tp.date.now("YYYY", -1) %>/<% tp.date.now("MM MMMM", -1) %>/<% tp.date.now("Do MMMM  YY - ddd", -1) %>|Previous day]] | [[Journal/Daily/<% tp.date.now("YYYY", 1) %>/<% tp.date.now("MM MMMM", 1) %>/<% tp.date.now("Do MMMM  YY - ddd", 1) %>|Next day]] >>

---
## 📅 Daily Questions

##### 🙌 What happened today that I'm grateful for...
- 

##### 🚀 Actions that moved me towards my goals...
- 

##### 🤔 Some changes I could make...
- 

---
## ✍ To-Do List
- [ ] 

---
## 📝 Today...
- <% tp.file.cursor() %>

---
### Notes created today
```dataview
List FROM "" WHERE file.cday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.ctime asc
```

### Notes last touched today
```dataview
List FROM "" WHERE file.mday = date("<%tp.date.now("YYYY-MM-DD")%>") AND file.cday != date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.mtime asc
```
