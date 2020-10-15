# OSTW Fragments
This repository is for short code that can be dropped into existing OSTW codebases.

Code here should be 
1. **single-purpose:** it should do one thing very well (e.g. a library for subscribeable events, or a macro that applies a smoothstep to a number between 0 and 1)
2. if necessary, **well-documented:** if something is long or the logic is not immediately obvious, it should be accompanied with explanations
3. **Your own** or **shared with permission**: pull requests made to this repo should contain code that you have express permission to share


## Macros
### Single-action Smoothstep
```cs
//edge0 is the point or value this will return at t=0
//edge1 is the point or value this will return at t=1
//t is a number between 0 and 1
//Follows a sigmoid curve
define SmoothStep(define edge0, define edge1, define t): edge0 + ((t^2)*(3-(2*t)))*edge1;
```
**Submitted by Protowalker**

---

### Single-action 2-point Bezier Curve
```cs
//p0-4 are the points that define the bezier path
//t is a number between 0 and 1
//Will follow a defined curve. The best way to generate these curves is via this desmos graph
//https://www.desmos.com/calculator/i5yegnlzrs
define BezierPathCalculation(Vector p0, Vector p1, Vector p2, Vector p3, define t): ((1-t)^3)*p0 + (3*(1-t)^2)*t*p1 + (3*(1-t)*(t^2)*p2) + (t^3)*p3;
```
**Submitted by Protowalker**

---
