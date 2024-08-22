::: mermaid

---

title: Ryu - Chart type

config:
  flowchart:
    nodeSpacing: 80
    rankSpacing: 50
  theme: dark
  themeVariables:
    nodeBorder: '#ccc'
---

graph LR
  %% Styling
  classDef lSpecial fill:#07a
  classDef mSpecial fill:#922
  classDef hSpecial fill:#922
  classDef od fill:#616
  classDef drc fill:#171,stroke-width:1.5px,stroke-dasharray: 10 7
  classDef dr fill:#171,stroke-width:1px
  classDef ch fill:#825
  classDef block fill:#444
  classDef super fill:#22b,stroke-width:2px
  classDef start fill:#008575
  classDef throw fill:#c61

    s1-jhk ---> s1-shk(s.HK) --> s1-cmk(c.MK) --x
      s1a-odpalm & s1b-hpalm
    s1a-odpalm --> s1a-shp(s.HP) --x s1a-hdp
    s1b-hpalm --> dr1 --x s1b-shp(s.HP) --x s1b-hdp

    s2-cmk --x drc1 --x s2-shp(s.HP)
    s2-shp --> s2-bhp(b.HP) --> s1a-odpalm & s1b-hpalm

    drc1[/DRC/]:::drc
    s1b-hdp{{H.DP}}:::hSpecial
    s1b-hpalm{{H.C-Palm}}:::hSpecial
    s1a-hdp{{H.DP}}:::hSpecial
    s1-jhk([j.HK]):::start
    s2-cmk([c.MK]):::start
    s1a-odpalm{{OD.C-Palm}}:::od

    dr1[/DR\]:::dr
:::
