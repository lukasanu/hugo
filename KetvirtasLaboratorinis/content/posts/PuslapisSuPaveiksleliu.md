---
title: "Puslapis su paveiksleliu ir kodu"
date: 2022-12-14T22:35:14+02:00
draft: true
---
![Paveikslelis](/Picture.png)
{{< highlight go "linenos=table,hl_lines=8 15-17,linenostart=199" >}}
func GetTitleFunc(style string) func(s string) string {
  switch strings.ToLower(style) {
  case "go":
    return strings.Title
  case "chicago":
    return transform.NewTitleConverter(transform.ChicagoStyle)
  default:
    return transform.NewTitleConverter(transform.APStyle)
  }
}
{{< / highlight >}}

