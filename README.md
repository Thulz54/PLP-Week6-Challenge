class Superhero:
    def __init__(self, name, superpower, level):
        self.name = name
        self.__superpower = superpower # Encapsulated attribute
        self.level = level

    def show_details(self):
        return f"{self.name} (Level {self.level}) has superpower: {self.__superpower}"

    def use_power(self):
        return f"{self.name} uses {self.__superpower}!"

class FlyingHero(Superhero):
    def __init__(self, name, superpower, level, flying_speed):
        super().__init__(name, superpower, level)
        self.flying_speed = flying_speed

    def use_power(self):
        return f"{self.name} flies at {self.flying_speed} km/h using {self._Superhero__superpower}!"

hero1 = Superhero("Shadow", "Invisibility", 5)
hero2 = FlyingHero("SkyRider", "Wind Blast", 7, 120)

print(hero1.show_details())
print(hero1.use_power())

print(hero2.show_details())
print(hero2.use_power())
class Vehicle:
    def move(self):
        pass # Generic move method

class Car(Vehicle):
    def move(self):
        return "Driving on the road!"

class Plane(Vehicle):
    def move(self):
        return "Flying in the sky!"

class Boat(Vehicle):
    def move(self):
        return "Sailing on water!"

vehicles = [Car(), Plane(), Boat()]

for v in vehicles:
    print(f"{v.__class__.__name__}: {v.move()}")
my_list = []
my_list.append(10)
my_list.append(20)
