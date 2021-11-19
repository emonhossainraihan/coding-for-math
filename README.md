## Mathematica

<details>
 <summary>Fixed point iteration</summary>

```
f[t_] := Cos[t];
g = Plot[{f[t], t}, {t, -\[Pi]/2, \[Pi]/2}, 
  AspectRatio -> 1, PlotStyle -> {Thick}, Epilog ->
   Module[{pts = NestList[f, .1, 10]},
    {
     Thin, PointSize[0.015],  
     Line@ Flatten[Map[{#, {#[[2]], #[[2]]}} &, Partition[pts, 2, 1], 1], 1],
     Red, Point[Partition[pts, 2, 1]]
     }
   ]
]    
```
</details>

<details>
 <summary>Fourier Transform of Piecewise function</summary>
 
```
FourierTransform[
 Piecewise[{{0, x < 0}, {Exp[-x], x > 0}}], x, \[Omega]]
```
</details>

 <details>
 <summary>Steps</summary>
  
 ```
 ShowSteps[exp_] := 
 WolframAlpha[
  ToString@HoldForm@InputForm@exp, {{"Input", 2}, "Content"}, 
  PodStates -> {"Input__Step-by-step solution"}]

SetAttributes[ShowSteps, HoldAll]
 ```
  
  </details>
 
## MatLab

## Fortran

