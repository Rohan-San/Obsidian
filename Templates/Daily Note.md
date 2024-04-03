---
created: <% tp.file.creation_date() %>
---
tags:: [[+Daily Notes]]

# <% moment().format("dddd, MMMM Do YYYY, h:mm:ss a") %>

<< [[Journal/Daily/<% tp.date.now("YYYY", -1) %>/<% tp.date.now("MM MMMM", -1) %>/<% tp.date.now("Do MMMM  YY - ddd", -1) %>|Previous day]] | [[Journal/Daily/<% tp.date.now("YYYY", 1) %>/<% tp.date.now("MM MMMM", 1) %>/<% tp.date.now("Do MMMM  YY - ddd", 1) %>|Next day]] >>

---
### 📅 Daily Questions
##### 🌜 Last night, after work, I...
- 

##### 🙌 One thing I'm excited about right now is...
- 

##### 🚀 One+ thing I plan to accomplish today is...
- [ ] 

##### 👎 One thing I'm struggling with today is...
- 

---
# 📝 Notes
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
