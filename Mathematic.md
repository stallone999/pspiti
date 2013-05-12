# Przykladowe cwiczenia z Mathematica
      
      
      In[85]:= (234 - 456)*(752 + 345)/((23 + 34)*(75 - 32) + (78*99))
      
      Out[85]= -(81178/3391)
      
      In[86]:= 34!
      
      Out[86]= 295232799039604140847618609643520000000
      
      In[87]:= 
      Sqrt[1 + 2 + 2^2 + 2^3 + 2^4 + 2^5]
      
      Out[87]= 3 Sqrt[7]
      
      In[88]:= 
      Sqrt[1 + 2 + 2^2 + 2^3 + 2^4 + 2^5]^(1/3)
      
      Out[88]= 3^(1/3) 7^(1/6)
      
      In[89]:= 
      (1 + 2 + 2^2 + 2^3 + 2^4 + 2^5)^(1/3)
      
      Out[89]= 3^(2/3) 7^(1/3)
      
      In[90]:= 
      Power[1 + 2 + 2^2 + 2^3 + 2^4 + 2^5, 1/3]
      
      Out[90]= 3^(2/3) 7^(1/3)
      
      
      (234.0 - 456)*(752 + 345)/((23 + 34)*(75 - 32) + (78*99))
      
      Out[91]= -23.9393
      
      In[92]:= 
      (234 - 456)*(752 + 345)/((23 + 34)*(75 - 32) + (78*99)) // N
      
      Out[92]= -23.9393
      
      In[93]:= 
      Sin[Pi/4]
      
      Out[93]= 1/Sqrt[2]
      
      In[94]:= 
      ArcSin[1/Sqrt[2]]
      
      Out[94]= \[Pi]/4
      
      In[97]:= 
      Sin[15*Pi/180]
      
      Out[97]= (-1 + Sqrt[3])/(2 Sqrt[2])
      
      In[98]:= 
      x^2 - 49
      
      Out[98]= -49 + x^2
      
      In[99]:= Solve[{x^2 - 49 == 0}]
      
      Out[99]= {{x -> -7}, {x -> 7}}
      
      In[100]:= 
      Solve[{x^2 + x - 6 == 0}]
      
      Out[100]= {{x -> -3}, {x -> 2}}
      
      In[101]:= 
      Solve[{(20*x^2) - (31*x) - 9 == 0}]
      
      Out[101]= {{x -> -(1/4)}, {x -> 9/5}}
      
      In[102]:= 
      Solve[{x^2 - (3*x) - 1 == 0}]
      
      Out[102]= {{x -> 1/2 (3 - Sqrt[13])}, {x -> 1/2 (3 + Sqrt[13])}}
      
      In[103]:= 
      Solve[{x^2 - (6*x) + 1 == 0}]
      
      Out[103]= {{x -> 3 - 2 Sqrt[2]}, {x -> 3 + 2 Sqrt[2]}}
      
      In[104]:= 
      Solve[{x^2 + (7*x) + 9}]
      
      During evaluation of In[104]:= Solve::naqs: 9+7 x+x^2 is not a quantified system of equations and inequalities. >>
      
      Out[104]= Solve[{9 + 7 x + x^2}]
      
      In[105]:= Solve[{x^2 + (7*x) + 9 == 0}]
      
      
      Out[105]= {{x -> 1/2 (-7 - Sqrt[13])}, {x -> 1/2 (-7 + Sqrt[13])}}
      
      In[106]:= 
      Solve[{x^2 + y^2 + (4*x*y) - 1 == 0}, {x, y}]
      
      During evaluation of In[106]:= Solve::svars: Equations may not give solutions for all "solve" variables. >>
      
      Out[106]= {{y -> -2 x - Sqrt[1 + 3 x^2]}, {y -> -2 x + Sqrt[
          1 + 3 x^2]}}
      
      In[107]:= 
      Solve[{x^2 + y^2 + (4*x*y) - 1 == 0}]
      
      Out[107]= {{x -> -2 y - Sqrt[1 + 3 y^2]}, {x -> -2 y + Sqrt[
          1 + 3 y^2]}}
      
      In[108]:= 
      Solve[{x^2 + y^2 + (4*x*y) - 1 == 0}, {x}]
      
      Out[108]= {{x -> -2 y - Sqrt[1 + 3 y^2]}, {x -> -2 y + Sqrt[
          1 + 3 y^2]}}
      
      In[109]:= 
      Solve[{x^2 + y^2 + (4*x*y) - 1 == 0}, {y}]
      
      Out[109]= {{y -> -2 x - Sqrt[1 + 3 x^2]}, {y -> -2 x + Sqrt[
          1 + 3 x^2]}}
      
      In[110]:= 
      Solve[{x^3 - x^2 + x + 1 == 0}]
      
      Out[110]= {{x -> 
         1/3 (1 - 2/(-17 + 3 Sqrt[33])^(1/3) + (-17 + 3 Sqrt[33])^(
            1/3))}, {x -> 
         1/3 + (1 + I Sqrt[3])/(3 (-17 + 3 Sqrt[33])^(1/3)) - 
          1/6 (1 - I Sqrt[3]) (-17 + 3 Sqrt[33])^(1/3)}, {x -> 
         1/3 + (1 - I Sqrt[3])/(3 (-17 + 3 Sqrt[33])^(1/3)) - 
          1/6 (1 + I Sqrt[3]) (-17 + 3 Sqrt[33])^(1/3)}}
      
      In[111]:= 
      r1 = x - (2*y) == 7
      r2 = x^2 + (4*y^2) == 37
      Solve[{r1, r2}, {x, y}]
      
      Out[111]= x - 2 y == 7
      
      Out[112]= x^2 + 4 y^2 == 37
      
      Out[113]= {{x -> 1, y -> -3}, {x -> 6, y -> -(1/2)}}
      
      In[114]:= 
      r1 = x + y == 1
      r2 = 16*x^2 + y^2 == 65
      Solve[{r1, r2}, {x, y}]
      
      Out[114]= x + y == 1
      
      Out[115]= 16 x^2 + y^2 == 65
      
      Out[116]= {{x -> -(32/17), y -> 49/17}, {x -> 2, y -> -1}}
      
      In[117]:= 
      r1 = y - x == a
      r2 = 2*x^2 + (x*y) + y^2 == 8
      Solve[{r1, r2}, {x, y}]
      
      Out[117]= -x + y == a
      
      Out[118]= 2 x^2 + x y + y^2 == 8
      
      Out[119]= {{x -> 1/8 (-3 a - Sqrt[128 - 7 a^2]), 
        y -> 1/8 (5 a - Sqrt[128 - 7 a^2])}, {x -> 
         1/8 (-3 a + Sqrt[128 - 7 a^2]), y -> 1/8 (5 a + Sqrt[128 - 7 a^2])}}
      
      In[120]:= 
      Sqrt1 = Sqrt[1 + Sqrt[x]]
      
      Out[120]= Sqrt[1 + Sqrt[x]]
      
      In[121]:= Sqrt2 = 2/(Sqrt[1 + x - (1/x)])
      
      Out[121]= 2/Sqrt[1 - 1/x + x]
      
      In[122]:= 
      wielomian = (3*x^3) + (2*x^2) + x + 1
      
      Out[122]= 1 + x + 2 x^2 + 3 x^3
      
      In[123]:= 
      ulamki = b + 1/(a + 1/x) + 1/(b + 1/(a + 1/x)) + 1/(
        c + 1/(b + 1/(a + 1/x)))
      
      Out[123]= b + 1/(c + 1/(b + 1/(a + 1/x))) + 1/(b + 1/(a + 1/x)) + 1/(
       a + 1/x)
      
      In[124]:= 
      duzoPierwiastków = Sqrt[a + Sqrt[a + Sqrt[a + Sqrt[a + Sqrt[x]]]]]
      
      Out[124]= Sqrt[a + Sqrt[a + Sqrt[a + Sqrt[a + Sqrt[x]]]]]
      
      In[125]:= 
      f[x_] = Sqrt[1 + Sqrt[2*x + 1]]
      
      Out[125]= Sqrt[1 + Sqrt[1 + 2 x]]
      
      In[126]:= 
      f[Sqrt[2]]
      
      Out[126]= Sqrt[1 + Sqrt[1 + 2 Sqrt[2]]]
      
      In[127]:= 
      f[Sqrt[3]]
      
      Out[127]= Sqrt[1 + Sqrt[1 + 2 Sqrt[3]]]
      
      In[128]:= 
      g[x_] = 1/Sqrt[(3*x^2) - 3*x + 5]
      
      Out[128]= 1/Sqrt[5 - 3 x + 3 x^2]
      
      In[129]:= g[Sqrt[2]]
      
      Out[129]= 1/Sqrt[11 - 3 Sqrt[2]]
      
      In[130]:= 
      g[Sqrt[3]]
      
      Out[130]= 1/Sqrt[14 - 3 Sqrt[3]]
      
      In[131]:= 
      h[x_] = x^4 + (2*x^2) + 4
      
      Out[131]= 4 + 2 x^2 + x^4
      
      In[132]:= 
      h[Sqrt[2]]
      
      Out[132]= 12
      
      In[133]:= 
      h[Sqrt[3]]
      
      Out[133]= 19
      
      In[134]:= 
      Fr[x_] = (1 + 1/(1 - 1/x))*1/(1 + 1/(1 - 1/x))
      
      Out[134]= 1
      
      In[135]:= 
      Fr[Sqrt[2]]
      
      Out[135]= 1
      
      In[136]:= 
      Fr[Sqrt[3]]
      
      Out[136]= 1
      
      In[137]:= 
      Rts[x_] = Sqrt[x - Sqrt[2*x + Sqrt[3*x - Sqrt[4*x + Sqrt[x]]]]]
      
      Out[137]= Sqrt[x - Sqrt[2 x + Sqrt[3 x - Sqrt[Sqrt[x] + 4 x]]]]
      
      In[138]:= 
      Rts[Sqrt[2]]
      
      Out[138]= Sqrt[Sqrt[2] - Sqrt[
       2 Sqrt[2] + Sqrt[3 Sqrt[2] - Sqrt[2^(1/4) + 4 Sqrt[2]]]]]
      
      In[139]:= 
      Rts[Sqrt[3]]
      
      Out[139]= Sqrt[Sqrt[3] - Sqrt[
       2 Sqrt[3] + Sqrt[3 Sqrt[3] - Sqrt[3^(1/4) + 4 Sqrt[3]]]]]
      
      In[140]:= 
      A = (2*x + 3)^2
      
      
      Out[140]= (3 + 2 x)^2
      
      In[141]:= 
      B = Expand[A]
      
      Out[141]= 9 + 12 x + 4 x^2
      
      In[142]:= 
      A = ((4*x^2) - 1)^2
      
      Out[142]= (-1 + 4 x^2)^2
      
      In[143]:= 
      B = Expand[A]
      
      Out[143]= 1 - 8 x^2 + 16 x^4
      
      In[144]:= 
      A = ((x - 1)^2)*((x - 4)^2)
      
      Out[144]= (-4 + x)^2 (-1 + x)^2
      
      In[145]:= 
      B = Expand[A]
      
      Out[145]= 16 - 40 x + 33 x^2 - 10 x^3 + x^4
      
      In[146]:= 
      A = ((x - 2)*(x - 3))^5*(x - 4)^2
      
      Out[146]= (-4 + x)^2 (-3 + x)^5 (-2 + x)^5
      
      In[147]:= 
      B = Expand[A]
      
      Out[147]= 124416 - 580608 x + 1234656 x^2 - 1581840 x^3 + 
       1359840 x^4 - 826280 x^5 + 363870 x^6 - 117005 x^7 + 27265 x^8 - 
       4490 x^9 + 496 x^10 - 33 x^11 + x^12
      
      In[148]:= 
      B = Simplify[A]
      
      Out[148]= (-4 + x)^2 (-3 + x)^5 (-2 + x)^5
      
      In[149]:= 
      B = Factor[A]
      
      Out[149]= (-4 + x)^2 (-3 + x)^5 (-2 + x)^5
      
      In[150]:= 
      Apart[A]
      
      Out[150]= 124416 - 580608 x + 1234656 x^2 - 1581840 x^3 + 
       1359840 x^4 - 826280 x^5 + 363870 x^6 - 117005 x^7 + 27265 x^8 - 
       4490 x^9 + 496 x^10 - 33 x^11 + x^12
      
      In[151]:= 
      A = (1 - x)^2
      
      Out[151]= (1 - x)^2
      
      In[152]:= 
      B = Expand[A]
      
      Out[152]= 1 - 2 x + x^2
      
      In[153]:= 
      A = (1 - x)^3
      
      Out[153]= (1 - x)^3
      
      In[154]:= 
      B = Expand[A]
      
      Out[154]= 1 - 3 x + 3 x^2 - x^3
      
      In[155]:= 
      A = (1 - x)^4
      
      Out[155]= (1 - x)^4
      
      In[156]:= 
      B = Expand[A]
      
      Out[156]= 1 - 4 x + 6 x^2 - 4 x^3 + x^4
      
      In[158]:= 
      A = (1 - x)^5
      
      Out[158]= (1 - x)^5
      
      In[159]:= 
      B = Expand[A]
      
      Out[159]= 1 - 5 x + 10 x^2 - 10 x^3 + 5 x^4 - x^5
      
      In[160]:=  A = (sin[x] + cos[x])^3
      
      
      Out[160]= (cos[x] + sin[x])^3
      
      In[161]:= 
      B = Expand[A]
      
      Out[161]= cos[x]^3 + 3 cos[x]^2 sin[x] + 3 cos[x] sin[x]^2 + sin[x]^3
      
      In[162]:= 
      A = ((1 + sin[x])/cos[x])^5
      
      Out[162]= (1 + sin[x])^5/cos[x]^5
      
      In[163]:= 
      B = Expand[A]
      
      Out[163]= 1/cos[x]^5 + (5 sin[x])/cos[x]^5 + (10 sin[x]^2)/
       cos[x]^5 + (10 sin[x]^3)/cos[x]^5 + (5 sin[x]^4)/cos[x]^5 + sin[x]^5/
       cos[x]^5
      
      In[164]:= 
      A = tan[x + 1]
      
      Out[164]= tan[1 + x]
      
      In[165]:= 
      B = Expand[A]
      
      In[166]:= tan[1 + x]
      
      Out[166]= tan[1 + x]
      
      In[167]:= 
      (2*x)^2 - (3*x)^3 == 0
      
      Out[167]= 4 x^2 - 27 x^3 == 0
      
      In[168]:= 
      (4*x)^4 - (5*x)^2 + 1 == 0
      
      Out[168]= 1 - 25 x^2 + 256 x^4 == 0
      
      In[169]:= 
      (9*x)^2 + (21*x) + 10 == 0
      
      Out[169]= 10 + 21 x + 81 x^2 == 0
      
      In[239]:= 
      Simplify[6*x^2 - 4*x - 4*x^3 + x^4 + 1]
      
      Out[239]= (-1 + x)^4
      
      In[171]:= 
      1/(y + 1)*(1/2*x + 1/2) + 1/(1 - y)*(1/2*x + 1/2)
      
      Out[171]= (1/2 + x/2)/(1 - y) + (1/2 + x/2)/(1 + y)
      
      In[188]:= 
      Simplify[1/(y + 1)*1/2*x + 1/2 + 1/(1 - y)*1/2*x + 1/2]
      
      Out[188]= (-1 - x + y^2)/(-1 + y^2)
      
      In[185]:= 
      Simplify[cos[x]*sin[y] + cos[y]*sin[x]]
      
      Out[185]= cos[y] sin[x] + cos[x] sin[y]
      
      In[186]:= 
      A = 5*x + 10*x^2 + 10*x^3 + 5*x^4 + x^5 + 1
      
      Out[186]= 1 + 5 x + 10 x^2 + 10 x^3 + 5 x^4 + x^5
      
      In[184]:= 
      B = Simplify[A]
      
      Out[184]= (1 + x)^5
      
      In[178]:= 1 + 5 x + 100 x^2 + 1000 x^3 + 625 x^4 + x^5
      
      
      Out[178]= 1 + 5 x + 100 x^2 + 1000 x^3 + 625 x^4 + x^5
      
      
      
      
      Out[179]= 1 + 5 x + 100 x^2 + 1000 x^3 + 625 x^4 + x^5
      
      
      
      
      In[197]:= AZ = (1/(y + 1))*(1/2*x + 1/2) + (1/(1 - y))*(1/2*x + 1/2)
      
      Out[197]= (1/2 + x/2)/(1 - y) + (1/2 + x/2)/(1 + y)
      
      
      
      In[198]:= B = Simplify[AZ]
      
      Out[198]= (1 + x)/(1 - y^2)
      
      In[201]:= 
      Manipulate[D[t^n, t], {n, 2, 10, 1}]
      
      Out[201]= Manipulate[D[t^n, t], {{n, 10}, 2, 10, 1}]
      
      In[202]:= 
      AC = (1 + 3*x)^5/(1 + 3*x)*(3 + 9*x)
      
      Out[202]= (1 + 3 x)^4 (3 + 9 x)
      
      In[203]:= 
      B = Simplify[AC]
      
      Out[203]= 3 (1 + 3 x)^5
      
      In[204]:= 
      AX = (Sqrt[2] - Sqrt[3])*(Sqrt[2] + Sqrt[3])
      
      Out[204]= (Sqrt[2] - Sqrt[3]) (Sqrt[2] + Sqrt[3])
      
      In[205]:= 
      B = Simplify[AX]
      
      Out[205]= -1
      
      In[207]:= 
      Simplify[(Sqrt[2] - Sqrt[3])*(Sqrt[2] + Sqrt[3])]
      
      Out[207]= -1
      
      In[209]:= 
      Apart[(x + 7)/(x^2 - x - 6)]
      
      Out[209]= 2/(-3 + x) - 1/(2 + x)
      
      In[210]:= 
      ((50*x^2 + 20*x + 6)/(x^3 + 2*x^2 + x))
      
      Out[210]= (6 + 20 x + 50 x^2)/(x + 2 x^2 + x^3)
      
      In[211]:= 
      Apart[(50*x^2 + 20*x + 6)/(x^3 + 2*x^2 + x)]
      
      Out[211]= 6/x - 36/(1 + x)^2 + 44/(1 + x)
      
      In[212]:= 
      Plot[Sin[t^3], {t, 0, 5}]
      
      Out[212]= \!\(\*
      GraphicsBox[{{}, {}, 
      {Hue[0.67, 0.6, 0.6], LineBox[CompressedData["
      1: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
      +gRfW3wcwk/TE8prrrGjfLtXGXmbWXz9a8CKiC07Kuh7YibHPoKLd3NvOGTH
      jpxTO2qF7EdwW6rzHrPb7Oi4C7sQT+sI5vlsdS3+ITtafZIU3PuRhqXkO51L
      H7Oj6qr+7ljuUXww+VwozZkd/ec9wbnHchRbfdL4q+jGjvhjgiUei9Lx820Z
      fec82VHr8xVPEXs6Dk3YvvzAix21pNz/rJ1PxyUf1in+8mNHt+SrK7ax+EOn
      jJdOdyDLP+ffQl4kA0/HrVqQQtmR3eeXBuk9DMwnff+JbDg7qlBRt5yRYGKZ
      WFqwznt2VLjupOwzUyZWk7zy5WY0OxrgqmagICY+F91Q9iaOHbnLarsrljGx
      jfjJ3vSP7KgoTUzqyBwTu0TmLzZ8YkfBcVo2rHmIw7eo/Defwo4CM78+SNQl
      cFpEssLmr+xog3Zjw5ADgcs2SR6Hb+wo9KaEr7Q/gbvDQ8wtfrCjfm5DiXOf
      CTy3kc/JPYsdTbNPvrL7TeA1b18EJeayo606btp2LQSW3TD7uRyzo1HRfqOT
      IwTWCL1Zyixk4TnueHCVxVeN1vd2C5Wwox0fzGdclwh8K9h4QfkPO9KWD95c
      z+K/busq15pUsCPjp1PFtBUCRwRq7nL6x8qfcjqoiMV/M4Qzj0XWsvDZpf/r
      whiBy/13XSloYEcB5x05PvcSuFcw7lF/MzuaI9X//FlN4IU3GwIp7ezIVa2l
      2JHFZ4XX+Kbs6GJHI1sFPzKjCLzdl1Ryqpcdeff9sNvwgsCI/1GXwwA7It87
      +3f6EoFNvJlzgcPsaPeM7IoHi5/a814T/jnKjnBjMq2Ch8AeXi07W5ns6ND1
      Zr4/rUz8/WWxmcQ0O7oXLLJEv8XEiSfKN3jOsfrrlorY351MHM5XW8tYZEcL
      3noeyf0M/Nyv61gOBwe6rMA/E6jNwHf1B9mkyBxo4PLrsE/jLH23jpH9ksqB
      otcXZHaH0LFu2IKCkSAHEnknY9daO4rhAvtI7loO9EvQ8Fe69ShW2swdJy3C
      gQQiBFabFmlYJPo/kfEtHOjgUfkkDWEa7k1QXH29kwNZ0T/NS1OHcYP1/qwJ
      BQ5kH68+wvmEpY93atw9r8SBik/GfcygDeLPX04OyR7kQJW/TXVrcwaw488b
      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
      8Lc+sIXEx43u37uZwfhFhxn7wkiZNdwoxiNrq7MUHSR5x69qCXOjVJF9F9we
      j4Lj4dNMjw3caNOGJQ12Mg3i2598S9jEjcyMXg1zq47Av4fJjmVi3IiZJrMp
      xWIYZFO5STxbudETwzunZAMHoU60SMRnDzcKba/synTqhZXv4+2flbnRmzQb
      zqOXe2DHWYnYqv3cqOXCH8801W547uksL6jBjYR11wRe/tEGClP7DweeYOVz
      k//tWGwNXHhzg5xxiuU//cWzkacK3HcEl9ef4UaX+H9tTMsvg/YrE4brjbnR
      g8P5QfpCueBVmWLz9io36nb0wDdKUvHAR8mgqCfcaCu1p/IWfwumu/XMk55z
      o6FNe487FrfhCYuYy1au3OjOsxLDmpudmE1ccuceL26UrXZAJvl3DyYvd/sF
      +3CjAL9MgaOrvZi/LXpm3u//+R7f+FqhH4uGShQWhnKjzKKjYRdtB7Hk/W45
      uXfcKIN6IdX34RDedi7a53UkN6oUbGMrfjCMFfZcmSRiuNGZhbCey1YjeN8a
      ifMGH1j5aHj5VZ6kYTVGV15mIus+kZ7IZxKjWLM8SmZLCjdSmK47PTYwinU+
      XfZ68YUbidxtIGLe0fEZT/GxgXRu9MVnQUX8MAMbX+8yPPGDGxkr6QUusvSC
      2ZGonNQsFp71rc5155n4muRlybW/uBHnnQ2/dVnz2XZVzPNhPuv3pgl163cR
      +E5HJ72tiBth6aVxmhOBHXMi9VEpK36jNhfvTAI/e2uWGf+XGwlI2Kj+6SWw
      x0MxMWoVN3prHaf3iKWffAw7XW/VcKNzoxyJz1j7Jmhv5EhNPStfW9XlP+ME
      Dhcy01Np5kbPPMqWztQQOIbY8j28jRsVvTxpviGSwImVHaKrndyoVsmOazdL
      P6Umv39+tZcbHSnWG0tl7cfvry4Nlg5wo7BDuhd/BTFxruUWXfkRbrTFkT/N
      S4SJi7Q60vzo3OhKfo27/ksG/iv9XmSaYP1euvnlxSE6rma/5Hx+khv5qg7Z
      zSrTcVPX5r5fM9ys/T7Y4HJ7FHf+aj8utcCNbil7SV5/T8P97yJSPZa5UVQF
      9axg1gieMN78WI+Tihj+csq/Cobw/L72rm8UKuLc3Sfc+GUQs62L0NrAS0Uj
      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
      4Erws9WJ2T34f9uuL34=
      "]]}},
      AspectRatio->NCache[GoldenRatio^(-1), 0.6180339887498948],
      Axes->True,
      AxesOrigin->{0, 0},
      PlotRange->{{0, 5}, {-0.9999999735683098, 0.9999998509371182}},
      PlotRangeClipping->True,
      PlotRangePadding->{
      Scaled[0.02], 
      Scaled[0.02]}]\)
      
      In[214]:= 
      Limit[(1 + 1/n)^n, n -> Infinity] // N
      
      Out[214]= 2.71828
      
      In[216]:= 
      Limit[Sin[x]/x, x -> 0] // N
      
      Out[216]= 1.
      
      In[217]:= 
      y = x^3 + x^2 + x + 1
      
      Out[217]= 1 + x + x^2 + x^3
      
      In[218]:= 
      D[y, x]
      
      Out[218]= 1 + 2 x + 3 x^2
      
      In[219]:= 
      Integrate[x^3 + x^2 + x + 1, x]
      
      Out[219]= x + x^2/2 + x^3/3 + x^4/4
      
      In[224]:= 
      yz = Sin[x] + Cos[x]
      
      Out[224]= Cos[x] + Sin[x]
      
      In[225]:= 
      D[yz, x]
      
      Out[225]= Cos[x] - Sin[x]
      
      In[226]:= 
      Integrate[Sin[x] + Cos[x], x]
      
      Out[226]= -Cos[x] + Sin[x]
      
      In[229]:= 
      yb = Tan[x] + Cos[x]
      
      Out[229]= Cos[x] + Tan[x]
      
      In[230]:= 
      D[yb, x]
      
      Out[230]= Sec[x]^2 - Sin[x]
      
      In[231]:= 
      Integrate[Tan[x] + Cos[x], x]
      
      Out[231]= -Log[Cos[x]] + Sin[x]
      
      In[232]:= 
      yu = E^(1 + x + x^2)
      
      Out[232]= E^(1 + x + x^2)
      
      In[233]:= 
      D[yu, x]
      
      Out[233]= E^(1 + x + x^2) (1 + 2 x)
      
      In[234]:= 
      Integrate[yu, x]
      
      Out[234]= 1/2 E^(3/4) Sqrt[\[Pi]] Erfi[1/2 + x]
      
      In[235]:= 
      yt = (1 + x)/(1 + x + x^2)
      
      Out[235]= (1 + x)/(1 + x + x^2)
      
      In[236]:= 
      D[yt, x]
      
      Out[236]= -(((1 + x) (1 + 2 x))/(1 + x + x^2)^2) + 1/(1 + x + x^2)
      
      In[237]:= 
      Integrate[yt, x]
      
      Out[237]= ArcTan[(1 + 2 x)/Sqrt[3]]/Sqrt[3] + 1/2 Log[1 + x + x^2]
      
      
