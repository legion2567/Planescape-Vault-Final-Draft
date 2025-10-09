---
tags:
  - Letter
aliases:
recipient:
sentTo:
sender:
sentFrom:
previousLetter:
nextLetter:
holder:
fc-calendar: Example Calendar
fc-category: Letter Delivery
fc-date: YYY-MM-DD
letterStatus:
summary: ""
---

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> # Details
> |  |  |
> |---|---|
> | **Previous Letter** | `VIEW[{previousLetter}][link]` |
> | **Next Letter** | `VIEW[{nextLetter}][link]` |
> | **Owner** | `VIEW[{holder}][link]` |
> | **Delivery Due Date** | `VIEW[{fc-date}]` |
> | **Status** | `VIEW[{letterStatus}]` |

# `=this.file.name`

## **To:** `VIEW[{recipient}][link]` **To Location:** `VIEW[{sentTo}][link]`

> <font color="#7f7f7f">Write the contents of the letter.</font>

- **From:** `VIEW[{sender}][link]`, **From Location:** `VIEW[{sentFrom}][link]`

## Notes



