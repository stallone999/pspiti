# Przykladowe cwiczenia z Mathematic

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

In[170]:= 
(6*x)^2 - 4*x - (4*x)^3 + x^4 + 1 == 0

Out[170]= 1 - 4 x + 36 x^2 - 64 x^3 + x^4 == 0

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
