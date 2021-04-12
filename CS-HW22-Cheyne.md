# C# Core Homework Chapter 22

---

**Cheyne Lowery**

**April 12, 2021**

**CS-HW22-Cheyne.md**

---

1. The difference between *associativity* and *precedence* is *associativity* is the *direction* of evaluation whereas *precedence* is the *order* of evaluation.

2. The difference between *binary* and *unary* operators is that *binary* operators require *two* operands, whereas *unary* operators only require *one* operand.

3. The four constrains imposed by C# with respoect to operator overloading are:
	1. The overloaded operator (method) must be declared as *public*.
	2. The operator must be declared as *static*.
	3. The operator must follow the original multiplicity constraints.
	4. At least one of the parameters must always be of the containing type.
	
4. The syntax for overloading an operater is:
```c#
	public static Object<T> operator operator<T> (Object<t> param1 AnyOther<T> param2) 
	{
	//body
	}
```

5. *Symmetric* overloaded binary operators are used to first, add two objects of different types, one being the of the containing type; and two, to make the custome operator more intuitive by overloading it making it evaluate the same way regardless of *associativity*.

6. You can only overload a *compound* assignment operator by overloading the operator on the custom type, in which it must be called as the original parameter. You *cannot* overload the compound assignment operator on a *build-in* type.

7. Overloading increment and decrement operators for *value types* will create a new object every time the overloaded operator is called. Conversely, calling an overloaded operator on a *reference type* will change the object to which it is called from.

8. We have to overload some operators in *pairs* due to the fact that the C# compiler enforces it, and there is a dichotemy/ dependency between two operators, *not equal to* cannot be evaluated without understanding *equal to*.

9. A *widening conversion* is a conversion to a type with *at least* as much information as the original type. A *narrowing conversion* is a conversion to a type with a *lesser amount* of information than the original type, and thus requires a *cast*.

10. An *explicit conversion* is a conversion from a type to a type that requries a *cast* due to the *loss of information*. An *implicit conversion* is a conversion from a type to a type that is handled by the compiler as there is no risk of losing information.