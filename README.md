# create-yourownclass
#plp assignment 
# Base class
class Superhero:
    def __init__(self, name, power, city):
        self.__name = name             # Encapsulation (private attribute)
        self.power = power
        self.city = city

    def get_name(self):
        return self.__name             # Encapsulation using getter

    def display_info(self):
        print(f"{self.__name} protects {self.city} with {self.power}.")

# Inherited class
class FlyingHero(Superhero):
    def __init__(self, name, power, city, flight_speed):
        super().__init__(name, power, city)  # Call to parent constructor
        self.flight_speed = flight_speed

    def display_info(self):
        print(f"{self.get_name()} flies over {self.city} at {self.flight_speed} km/h using {self.power}.")

# Create objects
hero1 = Superhero("Shadow", "Invisibility", "New York")
hero2 = FlyingHero("SkyBolt", "Thunderstorm", "Tokyo", 800)

# Call methods
hero1.display_info()
hero2.display_info()
