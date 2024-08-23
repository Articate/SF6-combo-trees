::: mermaid

---

title: Ryu - Game plan

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
  classDef mSpecial fill:#771
  classDef hSpecial fill:#922
  classDef od fill:#616
  classDef drc fill:#171,stroke-width:1.5px,stroke-dasharray: 10 7
  classDef dr fill:#171,stroke-width:1px
  classDef ch fill:#825
  classDef block fill:#444
  classDef super fill:#22b,stroke-width:2px
  classDef start fill:#008575
  classDef throw fill:#c61

  p([Pokes]):::start
  wp([Whiff punish]):::start
  md([Missed DP]):::start

  p --> p1-cmk(c.MK) --x drc1
    drc1 -. B-C .-> p1-shp(s.HP) --> p1-bhp(b.HP)
      p1-bhp -. Chg .-x p1-hpalm --> end1("...")
      p1-bhp -.-> p1-hdonkey -. Cnr .-> p1-ldp
    drc1 -. Blckd .-> p1-lp[[LP ...]]

  p --> p2-shp(s.HP)
  p2-shp -. B-C .-> p2-shk(s.HK) --x p2-charge
  p2-shp -.-> drc2 -- "+ on block" --> p2-shp2("s.HP") --> p2-bhk(b.HP)
  p2-bhk -.-> p2-hdp -.-> su3[[su3]]:::super
  p2-bhk -.-> p1-hdonkey

  wp --> p2-shp
  p2-shp -.-> wp-mtatsu

  md --> md-shk("(PC) s.HK") --> md-shp(s.HP)
    md-shp -.-> md-hdp
    md-shp -. Chg .-> m-odpalm --> m-d-shp(s.HP) --> mm("...")

  %% Pokes
  drc1[/DRC/]:::drc
  drc2[/DRC/]:::drc
  p1-hpalm{{H.C-Palm}}:::hSpecial
  p1-hdonkey{{H.Donkey}}:::hSpecial
  p1-ldp{{L.DP}}:::lSpecial
  p2-hdp{{H.DP}}:::hSpecial

  %% Whiff Punish
  wp-mtatsu{{Special}}:::mSpecial

  %% Missed DP
  md-hdp{{H.DP}}:::hSpecial
  m-odpalm{{OD.C-Palm}}:::od
  p2-charge[[Charge]]:::lSpecial
:::
