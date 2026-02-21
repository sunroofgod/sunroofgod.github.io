+++
title = 'OOP Thoughts on Mrt'
date = 2026-02-21T20:12:53+08:00
+++

in Design Patterns (1994) by GoF, they state early on that "prioritising object composition over inheritance" is ideal.

why? one reason is maintaibility - as more object classes get created, it'll be harder to change base classes that get
inherited by boatloads of other objects. in some sense, we're prioritising creation of mixin-like classes

another has to do with the nuanaces and (dis)advantages of inheritance of interfaces and implementations. unfortunately, 
im still trying to wrap my head around that right now.
