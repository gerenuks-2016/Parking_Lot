# Parking Lot

## Description

The information in this markdown is intended to expand on your questions we were not able to cover during lecture periods. It will also include best practices on how to approach programming. 

---

## Lecture Parking Lot

#### What the hell do the `dunders` mean

* `_name` vs `__name` vs `__name__`
* `_name` - If you see this, it means you shouldn't have access to this method. 
	* Similar to how programmers use `private methods` inside Ruby. 
* `__name` - This is used to indicate that this method should NOT be overridden by a subclass. 
* `__name__` - This is to tell you that these methods are being used by Python so don't create any with these names
* If you would like further examples of these three check out [this link](http://igorsobreira.com/2010/09/16/difference-between-one-underline-and-two-underlines-in-python.html)

#### Default Instance Variables in Classes

* When we instantiate a class we are creating a instance of that class
* Every instance can be unique with it's own unique variables. These are set using the `self` keyword
* You may recognize the example below

```
class Vehicle:
	def __init__(self, make, model, year):
		self.make = make
		self.model = model
		self.year = year

my_car = Vehicle("Bugatti", "Veyron", 2015)

my_car.make == "Bugatti"
my_car.year == 2015
```
* Now what happens if we want to set a `default value` to an instance variable
* We will assign it the default value inside the parenthesis where we declare our parameters

```
class Vehicle:
	def __init__(self, make, model, year = 2012):
		self.make = make
		self.model = model
		self.year = year

my_car = Vehicle("Bugatti", "Veyron")
my_car.year == 2012

your_car = Vehicle("Mazda", "Protege", 1990)
your_car.year = 1990
```
* Now every instance of that class will have a year set to `2012` UNLESS we decide to pass in an argument for `year`












