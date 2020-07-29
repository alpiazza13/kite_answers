headers:
    call-method: Call method
---
# How to call a method in a class in Python
A method defined within a class can be called on objects of that class. For example, if the function `say_hi(self)` is defined in a class `Speaker`, `say_hi` can be called on objects of type `Speaker`.

## Call a method on an object which belongs to the same class as the method {#call-method}
Call a method defined in a class on an instance of that class. In the code below, `Speaker` is a class which contains the function `say_hi`. The parameter `self` stands for the specific instance of `Speaker` on which `say_hi` is being called. Below, that instance is `new_speaker`.
```python
class Speaker:
    def say_hi(self):
        print("Hi!")
new_speaker = Speaker()
new_speaker.say_hi()
```

> **Further reading:**
> Object oriented programming is a common practice in Python. You can read more about it [here](https://realpython.com/python3-object-oriented-programming/).
