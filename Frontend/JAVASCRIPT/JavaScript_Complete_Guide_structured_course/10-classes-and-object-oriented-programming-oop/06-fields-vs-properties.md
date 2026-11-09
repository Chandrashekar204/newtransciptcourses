# 10.6 — Fields vs Properties

> Section 10: Classes & Object-oriented Programming (OOP)

So we learned these basics about classes, let me come back to that class field versus property thing because it is important to get that right. If you have a class that looks like this, then this here would be called a class field, this here when you will use it in the constructor would be called a class property right away, so title is a class property, category is a class field but it's important to know that in the end, this is just a theoretical separation, a field becomes a property, when we create an object based on the class, we just call it property in the constructor function right away because the constructor gets called during that object creation process so there we get a property right away.

You don't really have to memorize this difference though, in the end fields are like properties, we define them in a class so that we have a property when we create that object based on the class. The thing here at the bottom print info by the way would still be called a class method or an object method. In our code here, the implication is that all these things here in the constructor function are properties, of course I got fields of the same name which is no problem because these would be created as properties when we instantiate the product, now we basically overwrite everything we set up there in the constructor and therefore you can actually remove that.

This definition here is not required to be able to assign values, in the constructor you can add properties for the first time, so without having defined fields for them before just like that with the this keyword and indeed it makes no sense or it rarely makes sense to define fields here if you're assigning a value to them in the constructor right away anyways because then you just basically overwrite that default logic where every field would be translated to a property because you manually assign a value to that property and therefore add that property anyways in the constructor.

So this can be removed here, it's just something which will become important later again where we also work with fields which we don't initialize in the constructor. For now that's not the case, so our object can just look like this, our class can just look like this for the moment.

----------------------------------------
