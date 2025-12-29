---
title: "<% tp.file.title %>"
slug: "<% tp.file.title
  .toLowerCase()
  .replace(/[\s_]+/g, "-")
  .replace(/[^a-z0-9\-]/g, "") %>"

date: <% tp.date.now("YYYY-MM-DDTHH:mm:ss+08:00") %>
lastmod: <% tp.date.now("YYYY-MM-DDTHH:mm:ss+08:00") %>

author:
- CourageCheng

categories:
<%*
const cats = await tp.system.prompt(
  "输入 categories（逗号分隔）",
  "技术,后端"
);
if (cats) {
  cats.split(",").forEach(c => {
    tR += `- ${c.trim()}\n`;
  });
}
%>

tags:
<%*
const tags = await tp.system.prompt(
  "输入 tags（逗号分隔）",
  "Java,Hugo,Obsidian"
);
if (tags) {
  tags.split(",").forEach(t => {
    tR += `- ${t.trim()}\n`;
  });
}
%>

description: ""

weight:

draft: true

showToc: true
TocOpen: true
hidemeta: false
disableShare: true
showbreadcrumbs: true
mermaid: true

cover:
  image: ""
  caption: ""
  alt: ""
  relative: false
---
