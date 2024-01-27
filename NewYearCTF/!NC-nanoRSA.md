# nanoRSA

I didn't do a lot of crypto challenges, but this one was super easy and pretty funny too. 

We start with a text file with RSA information in it

```
e = 1
c = 9908255308151638808626355523286556242109836830117153917
n = 245841236512478852752909734912575581815967630033049838269083
```

This is pretty funny.

Ok, basically if e=1 there is NO encryption going on whatsoever. So that message c is literally just in "PLAINTEXT". Though we still need to decode it, and Long_to_bytes() will solve the flag in a split second for

grodno{R3sTcD4gH6iJ0kL}
