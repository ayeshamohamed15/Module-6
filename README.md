# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program

from abc import ABC, abstractmethod
  import math
  class Shape(ABC):
      @abstractmethod
      def calculate_area(self):
          pass
  class Rectangle(Shape):
      def _init_(self, length=1, breadth=1):
          self.length = length
          self.breadth = breadth
      def calculate_area(self):
          return self.length * self.breadth
  class Circle(Shape):
      def _init_(self, radius=1):
          self.radius = radius
      def calculate_area(self):
          return math.pi * self.radius ** 2
  rect = Rectangle(4, 5)
  circle = Circle(3)
  print("Rectangle Area:", rect.calculate_area())
  print("Circle Area:", circle.calculate_area())
  
## Output
![WhatsApp Image 2025-10-22 at 08 43 49_61e30eb4](https://github.com/user-attachments/assets/d1c325f5-609c-4f66-8380-4da422392cb7)

## Result
Thus,the program is verified successfully.
# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
class Rectangle:
      def _init_(self, length, breadth):
          self.__length = length
          self.__breadth = breadth
          print("Length:", self.__length)
          print("Breadth:", self.__breadth)
  
  rect = Rectangle(10, 5)  class Rectangle:
      def _init_(self, length, breadth):
          self.__length = length
          self.__breadth = breadth
          print("Length:", self.__length)
          print("Breadth:", self.__breadth)
  
  rect = Rectangle(10, 5)
## Output
![WhatsApp Image 2025-10-22 at 08 43 50_c30792a5](https://github.com/user-attachments/assets/6bdb0e47-16ef-432a-98c1-9c900d127f20)

## Result
Thus the program is verified succesfully.
# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
    def type(self):
        print("shark")

obj_goldfish = Fish()
obj_hammerhead = Shark()

for fish in (obj_goldfish, obj_hammerhead):
    fish.type()

## OUTPUT
![WhatsApp Image 2025-10-22 at 08 43 51_b3d348a9](https://github.com/user-attachments/assets/cd919478-5c5e-4e81-8b1d-3037f7a7d135)

## RESULT
Thus,the program is verified successfully.
# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
class A:
      def _init_(self,value):
          self.value=value
      def _lt_(self,other):
          if isinstance(other,A):
              return self.value<other.value
          return NotImplemented
  ob1=A(20)
  ob2=A(10)
  if ob2<ob1:
      print("ob2 is less than ob1")
  else:
      print("ob1 is less than ob2")
## Output
![WhatsApp Image 2025-10-22 at 08 43 51_31f272c8](https://github.com/user-attachments/assets/6f99344f-4ee9-4288-984f-5ee4b5661388)

## Result
Thus,the program is verified successfully.
# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
class Beans(): 
       def type(self): 
         print("Vegetable") 
       def color(self):
         print("Green") 
  class Mango(): 
       def type(self): 
         print("Fruit") 
       def color(self): 
         print("Yellow")      
  def func(obj): 
      obj.type()
      obj.color()
  obj_Beans=Beans()
  obj_mango=Mango()
  func(obj_Beans) 
  func(obj_mango)
## Output
![WhatsApp Image 2025-10-22 at 08 43 52_20184d89](https://github.com/user-attachments/assets/e139a16b-a9ea-4a1f-bf04-645403d9a107)

## Result
Thus the program was verified successfully.
