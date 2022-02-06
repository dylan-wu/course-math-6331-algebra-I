---
description: Final exam
owner:
type: project
subType: exam
priority: High, Medium, Low
tags:
parent:
  - course-math-6331-algebra-i
due:
  - May
---

```dataviewjs
linksTable("links")

//==========Library Code=========================
// linksTable:v2
function linksTable(field="links"){
    let links = parseLinks(dv.current()[field])
    if(links && links.length){
        dv.span('<h2 style="display:inline">Links: </h2')
        dv.span(links.map((l, i)=>{
            if (l.url.startsWith("http://") || l.url.startsWith("https://")){
                return `<a href="${l.url}" class="exteral-link" rel="noopener">${l.title?l.title:l.url}</a>`
            } else {
                return `[[${l.url}]]`
            }
        }).join(" | "))
    }}
function parseLinks(links){
    /**
    let links = parseLinks(dv.current().links)
    if(links && links.length){
        dv.table(["Title", "URL"], 
            links
            .map(l=>[
                l.title,
                l.url
            ]))
    }
    */
    links = links && links.values && links.values!=0 && links.map(l=>{
        if(typeof(l) == "string"){
            return {url: l}
        } else {
            let key = Object.keys(l)[0]
            let value = l[key]
             if(key == "twitter" && l[key] && !l[key].startsWith("http")){
                value = `https://twitter.com/${l[key]}`
            }
            return {title: key, url: value}
        }
    })
    if (!links) links = []
    return links.filter(a=>a.url)}
```



## Related
```dataviewjs
relatedTable("project")
relatedTable("task")
relatedTable("note")
relatedTable("source")
relatedTable("model")
relatedTable("topic")
relatedTable("list")

// library functions =====================================
function relatedTable(type="task"){
    let lookup = {
        "task": {relation:"project", header:"Tasks"},
        "project": {relation:"parent", header:"Subprojects"},
        "note": {relation:"project", header:"Notes"},
        "source": {relation:"source", header:"Sources"},
        "model": {relation:"model", header:"Examples"},
        "topic": {relation:"topic", header:"References"},
        "list": {relation:"list", header:"Listicals"}
    }
    let filter = lookup[type] 
    let pages = dv.pages('-"!"').where(p=>p[filter.relation] && p[filter.relation].includes(dv.current().file.name))
    if(pages.length){
        header(3, `${filter.header} (${pages.length})`)
        dv.table(["File", "Tasks", "Completed", "Tags", "Comment"], 
            pages
            .map(p => [
                iLink(p.file.path, properName(p)),
                p.file.tasks.filter(t=>t.fullyCompleted==false).length?p.file.tasks.filter(t=>t.fullyCompleted==false).length:"",
                p.file.tasks.filter(t=>t.fullyCompleted==true).length?p.file.tasks.filter(t=>t.fullyCompleted==true).length:"",
                p.file.tags,
                p.comment
            ]))
    }}
function header(level, title){
    dv.paragraph(`<div><h${level} data-heading=${title}><div class="heading-collapse-indicator collapse-indicator collapse-icon"><svg viewBox="0 0 100 100" class="right-triangle" width="8" height="8"><path fill="currentColor" stroke="currentColor" d="M94.9,20.8c-1.4-2.5-4.1-4.1-7.1-4.1H12.2c-3,0-5.7,1.6-7.1,4.1c-1.3,2.4-1.2,5.2,0.2,7.6L43.1,88c1.5,2.3,4,3.7,6.9,3.7 s5.4-1.4,6.9-3.7l37.8-59.6C96.1,26,96.2,23.2,94.9,20.8L94.9,20.8z"></path></svg></div>${title}</h${level}></div>`)}
function iLink(href, text=null){
	if (!href){
		if (typeof text === 'string' || text instanceof String)
		{
			if(text.startsWith("#")){
				return `${text}`
			}
			else{
				return `[[${text}]]`
			}
		} else {
			return text
		}
	}
	return `<a href="${href}" class="internal-link" rel="noopen">${text}</a>`}
function iListLink(list){
	return list && list.map && list.map(e=>iLink(null, e)).join("<br/>")}
function properName(p){
	return p.title?p.title:(p.alias?p.alias:p.file.name)}
```
