# Carbon-Emissions-calculator-for-transportation-
# Carbon emission calculator for transportation

# Define emission factors (in kg CO2 per km) for different modes of transportation
emission_factors = {
    'car': 0.2,     # Average for petrol cars
    'bus': 0.03,    # Average for urban buses
    'train': 0.04,  # Average for passenger trains
    'bicycle': 0,   # Assuming bicycles have no carbon emissions
    'walking': 0    # Assuming walking has no carbon emissions
}

print("Welcome to the Carbon Emission Calculator for Transportation!")
mode = input("Enter your mode of transportation (car/bus/train/bicycle/walking): ").lower()
distance = float(input("Enter the distance traveled in kilometers: "))

if mode in emission_factors:
    emission_factor = emission_factors[mode]
    emission = emission_factor * distance
    print(f"Carbon emissions for traveling {distance} km by {mode}: {emission} kg CO2")
else:
    print("Invalid mode of transportation. Please try again.")
