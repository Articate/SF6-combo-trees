::: mermaid

---

title: Ryu - Ideas

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

  classDef od fill:#154
  classDef drc fill:#171,stroke-width:2px
  classDef dr fill:#171,stroke-width:1px
  classDef ch fill:#828
  classDef block fill:#444
  classDef super fill:#22b,stroke-width:2px
  classDef start fill:#279
  classDef special fill:#595
  classDef hSpecial fill:#922
  classDef mSpecial fill:#992
  classDef lSpecial fill:#299

  adv("-30 adv."):::start --> hdonkey --> su1
  cmk("c.MK") --x drc1 --x shp(s.HP) --> bhp(b.HP) --x hcpalm & odcpalm
  hcpalm --> mtatsu -. corner .-> spec
  odcpalm -->
    shp2(s.HP) --x spec2
    shp2 -. corner .-> odtatsu -.-> hdp

  pc[["(PC) s.HK"]]:::start --> shp3(s.HP) --x odcpalm2{{OD.C-Palm}}:::od --> sph3(s.HP) --x odtatsu2{{OD.Tatsu}}:::od --> dr1[/DR\]:::dr --> smp(s.MP) --x drc2[/DRC/]:::drc --> chp(c.HP) --x mdonkey{{M.Donkey}}:::mSpecial --> hdp2{{H.DP}}:::hSpecial --x su3[[su3]]:::super

  %%hdp2{{H.DP}}:::hSpecial
  %%mdonkey{{M.Donkey}}:::mSpecial
  %%dr1[/DR\]:::dr
  %%odtatsu2{{OD.Tatsu}}:::od
  %%odcpalm2{{OD.C-Palm}}:::hSpecial
  %%drc2[/DRC/]:::drc
  hdp{{H.DP}}:::hSpecial
  odtatsu{{OD.Tatsu}}:::od
  spec{{Special}}:::special
  spec2{{Special}}:::special
  mtatsu{{M.Tatsu}}:::mSpecial
  odcpalm{{OD.C-Palm}}:::od
  hcpalm{{H.C-Palm}}:::hSpecial
  drc1[/DRC/]:::drc
  su1[[su1]]:::super
  hdonkey{{H.Donkey}}:::hSpecial

:::
