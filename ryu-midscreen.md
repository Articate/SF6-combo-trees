::: mermaid
---
title: Ryu - Midscreen
---
graph LR
    
	s1([j.HK]) -->
		f1(s.HK) --> 
        f1b(c.MK) --x
            f1-1{{H.DP}}
        f1b --x
            drc1

    drc1[/DRC/]
	drc1 --x
		s1-c1(s.HK) --> s1-c1b(s.HP) --x s1-c1c>OD.Donkey] --o
		    r3-e(b.HK) -->
                r4{{H.DP}} --x
                r4-1[[su3]]
		    r3-e --x 
			    r5[[su1]]
    drc1 --x
        s1-c2(s.HP) --> 
        s1-c2b(b.HP)--x
            s1-c2-1{{H.Donkey}} & s1-c2-2{{H.DP}}

	%% Poke
	s2([c.MK]) ---x
	    drc2[/DRC/] -.->
        drc2d{Block} -. no .->
            s1-c2
        drc2d -. yes .->
            p1[[s: s/c.LP]]
	    

	%% Others
    s3([c.MP]) -.->
        d1{CH?} -. Yes .->
            d1-y(c.MP) --x d2-yb(M.Donkey)

	s4([s / c.LP]) -.->
        d2{CH?} -. No .->
            d2-n(LP) -->
            d2-nb(LP) --x
            d2-nc(L.Tatsu)
        d2 -. Yes .->
            d1-y(c.MP)
:::