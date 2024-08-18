::: mermaid
---
title: Ryu - Corner
---
graph LR
	c_s1([j.HK])

	c_s1 -->
		c_s1-1(s.HK) -->
		c_s1-1-1(c.MK) -->
			c_r1(OD.Tatsu)
			c_r1 -->
			c_r1-1[H.DP]
			c_r1 --> 
			c_r1-2(DR) -.-> c_r1_2-1(s.MP) -.-> c_r1_2-2(M.Palm) -.-> c_r1-2-2(H.DP)
		c_s1-1-1 -->
			c_r3
	c_s1 -->
		c_s1-2(s.HP) --> c_r3
	c_s1 -->
		c_s1-3(b.HP) --> c_r2
		
		c_r2(H.Donkey) --> c_r2-1(L.DP)
		c_r3(DRC) -->
		c_r3-1(s.HP) --> c_r3-1-1(b.HP) -.-> c_r3-1-2(H.Donkey) --> c_r3-1-3(L.DP)
		c_r3 -->
		c_r3-2(s.HK) --> c_r3-2-1(s.HP) -.-> c_r3-2-2(OD.Tatsu)
		c_r3-2-2 -->
			Odin
		c_r3-2-2 -->
			c_r3-2-2-2(H.DP)
:::