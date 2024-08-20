::: mermaid
---
title: Ryu - Optimal combo tree
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
	classDef special fill:#922
	classDef od fill:#777700
	classDef drc fill:#171,stroke-width:2px
	classDef dr fill:#171,stroke-width:1px
	classDef ch fill:#828
	classDef block fill:#444
	classDef super fill:#22b,stroke-width:2px
	classDef start fill:#279

	ch_s1([j.HK]) --> ch_r1(s.HK)
	ch_r1 --> ch_r1-2(c.MK)
	ch_r1-2 -.-> |2 dg| ch_r1-3(OD.C-Palm)
	ch_r1-3 --> ch_r1-4(s.HP)
	ch_r1-4 -.-> |3 dg| ch_r1-e(DRC)
	ch_r1-e -.-> ch_r2(s.HP)
	ch_r2 --> ch_r2-2(b.HP)
	ch_r2-2 -.-> ch_r2-3(H.DP)
	ch_r1-e -.-> ch_r3(s.HK)
	ch_r3 --> ch_r3_2(s.HP)
	ch_r3_2 -.-> |2	 dg| ch_r3_3(OD.Donkey)
	ch_r3_3 --> ch_r3_4(b.HK)
	ch_r3_4 -.-> chr3_5(H.DP)
:::