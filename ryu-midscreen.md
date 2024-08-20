::: mermaid
---

title: Ryu - Optimal combo tree
config:
  flowchart:
    nodeSpacing: 70
    rankSpacing: 50
  theme: dark
  themeVariables:
    nodeBorder: '#ccc'
---

graph LR
  %% Styling
  classDef special fill:#922
  classDef od fill:#777700
  classDef drc fill:#171,stroke-width:2px
  classDef dr fill:#171,stroke-width:1px
  classDef ch fill:#828
  classDef block fill:#444
  classDef super fill:#22b,stroke-width:2px
  classDef start fill:#279

  m([Midscreen])
  mc([Mid, chg])

  m --> m1-jhk
  m --> m2-cmk
  m --> m3-lp

  m1-jhk --> m1-shk(s.HK) --> m1-cmk(c.MK) --x m1-hdp & drc1
    drc1 --x m1a-shk(s.HK) & m1b-shp(s.HP)
      m1a-shk --> m1a-shp(s.HP) --x m1a-oddonkey --o m1a-bhk(b.HK) --x m1a-hdp{{H.DP}} & m1a-su1
        m1a-hdp --x m1a-su3
      m1b-shp --> m1b-bhp(b.HP)--> m1b-hdp

  m2-cmk([c.MK]) ---x drc2 --o
    block1 -. No .-x m1b-shp
    block1 -. Yes .-x test[[c.LP ...]]
    block1 -. Mix .-x throw1

  m3-lp -.->
    ch1 -. No .-> ch1-n-lp1(LP) --> ch1-n-lp2(LP) --> ch1-n-tatsu
    ch1 -. Yes .-> ch1-y-cmp(c.MP)

  mc --> mc1-jhk --> mc1-shk(s.HK) --> mc1-cmk(c.MK) --x
    mc1a-odpalm & mc1b-hpalm

  mc1a-odpalm --> mc1a-shp(s.HP) --x mc1a-hdp
  mc1b-hpalm --> dr1 --x mc1b-shp(s.HP) --x mc1b-hdp

  mc --> mc2-cmk

  throw1[\Throw/]:::throw
  ch1-n-tatsu{{L.Tatsu}}:::special
  mc1b-hdp{{H.DP}}:::special
  mc1b-hpalm{{H.C-Palm}}:::special
  mc1a-hdp{{H.DP}}:::special
  mc1-jhk([j.HK]):::start
  mc2-cmk([c.MK]):::start
  mc1a-odpalm{{OD.C-Palm}}:::od
  m1-jhk([j.HK]):::start
  m2-cmk([c.MK]):::start
  m3-lp([c / s.LP]):::start
  ch1{CH?}:::ch
  m1a-su3[[su3]]:::super
  m1a-su1[[su1]]:::super
  m1-hdp{{H.DP}}:::special
  drc1[/DRC/]:::drc
  drc2[/DRC/]:::drc
  dr1[/DR\]:::dr
  m1a-oddonkey{{OD.Donkey}}:::od
  m1a-hdp{{H.DP}}:::special
  m1b-hdp{{H.DP}}:::special
  block1{Block?}:::block
:::
