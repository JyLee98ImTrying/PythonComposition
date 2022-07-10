# PythonComposition
# Learn how to do compositions in Python Object Oriented Programming
#We can use Is/Are Rules, what if we dont have rules that is not a class of the parent? 
# we can call their method 
#  why we are adding the dictionary in the constructor instead of directly to the class.
#  we do this to make sure Each instance will have its own list independent of the others. 
# Rule of Thumb: Alwasy initialise mutable attributes in the constructor. 

class Repository: 

class Clothing:
   stock={ 'name': [],'material' :[], 'amount':[]}
   def __init__(self,name):
     material = ""
     self.name = name
   def add_item(self, name, material, amount):
     Clothing.stock['name'].append(self.name)
     Clothing.stock['material'].append(self.material)
     Clothing.stock['amount'].append(amount)
   def Stock_by_Material(self, material):
     count=0
     n=0
     for item in Clothing.stock['material']:
       if item == material:
         count += Clothing.stock['amount'][n]
         n+=1
     return count
   def Stock_by_item(self, name):
     count=0
     n=0
     for rec in Clothing.stock['name']:
       if rec == name:
         count += Clothing.stock['amount'][n]
         n+=1
     return count
     class shirt(Clothing):
   material="Cotton"

class pants(Clothing):
   material="Cotton"

polo = shirt("Polo")
other_polo_shirts = shirt("Polo")

sweatpants = pants("Sweatpants")
polo.add_item(polo.name, polo.material, 4)
other_polo_shirts.add_item(other_polo_shirts.name, other_polo_shirts.material, 16)

sweatpants.add_item(sweatpants.name, sweatpants.material, 6)
current_stock = polo.Stock_by_item("Polo")
print(current_stock)

