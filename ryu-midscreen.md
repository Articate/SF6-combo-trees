::: mermaid

---

title: Ryu - Corner

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

  m1-jhk --> m1-shk(s.HK) --> m1-cmk(c.MK) --x m1-hdp & drc1
    drc1 --x m1a-shk(s.HK) & m1b-shp(s.HP)
      m1a-shk --> m1a-shp(s.HP) --x m1a-oddonkey --o m1a-bhk(b.HK) --x m1a-hdp{{H.DP}} & m1a-su1
        m1a-hdp --x m1a-su3
      m1b-shp --> m1b-bhp(b.HP)--> m1b-hdp

  m2-cmk([c.MK]) ---x drc2 --o
    block1 -. No .-x m1b-shp
    block1 -. Yes .-x external([c.LP ...]):::start
    block1 -. Mix .-x throw1

  m3-lp -.->
    ch1 -. No .-> ch1-n-lp1(LP) --> ch1-n-lp2(LP) --> ch1-n-tatsu
    ch1 -. Yes .-> ch1-y-cmp(c.MP)

  throw1[\Throw/]:::throw
  ch1-n-tatsu{{L.Tatsu}}:::lSpecial
  m1-jhk([j.HK]):::start
  m2-cmk([c.MK]):::start
  m3-lp([c / s.LP]):::start
  ch1{CH?}:::ch
  m1a-su3[[su3]]:::super
  m1a-su1[[su1]]:::super
  m1-hdp{{H.DP}}:::hSpecial
  drc1[/DRC/]:::drc
  drc2[/DRC/]:::drc
  m1a-oddonkey{{OD.Donkey}}:::od
  m1a-hdp{{H.DP}}:::hSpecial
  m1b-hdp{{H.DP}}:::hSpecial
  block1{Block?}:::block
:::
