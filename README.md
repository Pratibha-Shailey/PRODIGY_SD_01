# PRODIGY_SD_01
Easily convert between Celsius, Fahrenheit, and Kelvin with this user-friendly command-line tool. Open-source and versatile for various temperature-related tasks.
<br>
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def celsius_to_kelvin(celsius):
    return celsius + 273.15

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def fahrenheit_to_kelvin(fahrenheit):
    return (fahrenheit - 32) * 5/9 + 273.15

def kelvin_to_celsius(kelvin):
    return kelvin - 273.15

def kelvin_to_fahrenheit(kelvin):
    return (kelvin - 273.15) * 9/5 + 32

def main():
    print("Temperature Conversion Program")
    temperature = float(input("Enter temperature value: "))
    original_unit = input("Enter the original unit of measurement (C/F/K): ").upper()

    if original_unit == 'C':
        fahrenheit = celsius_to_fahrenheit(temperature)
        kelvin = celsius_to_kelvin(temperature)
        print(f"{temperature}°C is equal to {fahrenheit:.2f}°F and {kelvin:.2f}K")
    elif original_unit == 'F':
        celsius = fahrenheit_to_celsius(temperature)
        kelvin = fahrenheit_to_kelvin(temperature)
        print(f"{temperature}°F is equal to {celsius:.2f}°C and {kelvin:.2f}K")
    elif original_unit == 'K':
        celsius = kelvin_to_celsius(temperature)
        fahrenheit = kelvin_to_fahrenheit(temperature)
        print(f"{temperature}K is equal to {celsius:.2f}°C and {fahrenheit:.2f}°F")
    else:
        print("Invalid input. Please enter C, F, or K as the original unit.")

if __name__ == "__main__":
    main()

