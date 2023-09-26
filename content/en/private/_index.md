---
title: Private Area (For Instructors)
# cms_exclude: true

_build:
  render: always
  list: never
---

## Contents

- [Setup for instructors]({{< ref "private/setup" >}})
- [Grading Poll Project Part 1]({{< ref "private/part1" >}})

## To bulk delete from powershell

```powershell
Get-Content repos_names.txt | ForEach-Object { gh repo delete --yes $_ }
```

repo_names.txt: contains names of repos to be delted
