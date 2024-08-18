::: mermaid
---
title: Ryu
---
graph LR
 subgraph normal [No Charge]
    direction LR
    %% Jump Start
    s1[j.HK Normal] -->
        r1[s.HK] -->
        r1-e[c.MK] -.->
          r2[H.DP]
        r1-e -. 3 dg .->
          r3

    r3[DRC] -.->
        r3-1[s.HK] --> 
        r3-2[s.HP] -.2 dg.-> 
        r3-3[OD.Donkey] -->
        r3-e[b.HK] -.->
          r4[H.DP] -.3 sg.->
          r4-1[su3]
        r3-e -.1 sg.-> 
          r5[su1]

    %% Poke
    s2[c.MK] -.->
    s2_1[DRC] -.->
    r6[s.HP] -->
    r6_1[b.HP]

    %% Others
    s3[s/c.LP] -->
    d1{CH} -->
      |No| d1-1[s/c.LP] -->
      d1-1-2[s/c.LP] -.->
      d1-1-3[L.Tatsu]
    d1 -->
      |Yes| d1-2[c.MP] -.->
      d1-2-2[M.Donkey]
    
  end

  subgraph charged [Charged]
    direction LR
    ch_s1[j.HK Charged] --> ch_r1[s.HK]
    ch_r1 --> ch_r1-2[c.MK]
    ch_r1-2 -.-> |2 dg| ch_r1-3[OD.C-Palm]
    ch_r1-3 --> ch_r1-4[s.HP]
    ch_r1-4 -.-> |3 dg| ch_r1-e[DRC]
    ch_r1-e -.-> ch_r2[s.HP]
    ch_r2 --> ch_r2-2[b.HP]
    ch_r2-2 -.-> ch_r2-3[H.DP]
    ch_r1-e -.-> ch_r3[s.HK]
    ch_r3 --> ch_r3_2[s.HP]
    ch_r3_2 -.-> |2  dg| ch_r3_3[OD.Donkey]
    ch_r3_3 --> ch_r3_4[b.HK]
    ch_r3_4 -.-> chr3_5[H.DP]
  end
  :::