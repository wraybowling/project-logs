---
---
I started to wonder recently just how deep the calc() function in CSS could go. Let's consider a simple case:

- at 400px wide I want the text to be 13pt
- at 800px wide I want the text to be 18pt

Can the CSS calculator handle this in a semantic (if verbose) way? Let's find out. We know that it's possible to use calc to establish a value that adds or subtracts scalars and static values in the same scope. That's essentially the same as simple algebraic form of the standard linear function y=a*x+b.

If we already knew the slope and offset of the function it would be as simple as calc(a +b) but the point of this exercise is that *I don't want to think about the math ahead of time. I have a freaking calculator right here, right? Shouldn't it be able to do the work?* Sort of. We'll have to do some algebra first. We need an equation that takes all four values and makes up a function that equals the same slope and offset.

the first problem we crash into is the fact that pixels and points are completely different unit systems. So... unit conversion. Blech. But.... the function we need is rise over run which means that CSS will resolve pure units and we don't need to think about it. Yay!

```
calc( (18pt - 13pt) / (800px - 400px) );
```

But this doesn't work. This will just always compute the viewport width. And in even nicer situations, I recommend using viewport min which will choose the smaller of the two.

(to be continued)
