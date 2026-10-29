### Ex-05: Develop a Population Growth Model
## NAME : LIVYA DHARSHINI G
## REGISTER NUMBER : 2305001013
## Aim
To develop a simple mathematical model for population growth using Python and predict the
population for future years.
## Objectives

1. To enter and display population data.
   
2. To plot the population growth over time.
   
3. To develop a linear population growth model.
   
4. To calculate actual and predicted population values.
   
5. To predict future population and visualize the growth trend.

## program 
```
import numpy as np
import matplotlib.pyplot as plt
year = np.array([2020, 2021, 2022, 2023, 2024])
population = np.array([10000, 10500, 11000, 11600, 12000])
print("Years:", year)
print("Population:", population)
plt.figure(figsize=(8, 4))
plt.plot(year, population, marker='o', label='Actual')
plt.title("Population Growth")
plt.xlabel("Year")
plt.ylabel("Population")
plt.grid(True)
plt.legend()
plt.show()
t = np.array([0, 1, 2, 3, 4])
b, a = np.polyfit(t, population, 1)
predicted = a + b * t
print("Starting Population (a) =", round(a, 2))
print("Growth per Year (b) =", round(b, 2))
print("\nYear | Actual | Predicted")
for i in range(len(year)):
  print(year[i], "|", population[i], "|", round(predicted[i], 2))
  future_year = np.array([2025, 2026, 2027])
future_t = np.array([5, 6, 7])
future_population = a + b * future_t

print("Future Population Forecast")
for i in range(len(future_year)):
    print(f"{future_year[i]}: {future_population[i]:.2f}")
    plt.figure(figsize=(9, 5))
plt.plot(year, population, marker='o', label='Actual')
plt.plot(year, predicted, marker='x', linestyle='--', label='Model')
plt.plot(future_year, future_population, marker='s', linestyle=':', label='Forecast')
plt.title("Population Growth Model")
plt.xlabel("Year")
plt.ylabel("Population")
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.show()
```

## Output

<img width="781" height="652" alt="image" src="https://github.com/user-attachments/assets/f77ec7ae-b0c9-4683-9990-e5ec00619ad3" />



<img width="848" height="472" alt="image" src="https://github.com/user-attachments/assets/b119a8a6-4935-49fd-b73f-3fd64106acf0" />

## Result

A simple linear population growth model was successfully developed using Python. The model was
used to calculate predicted population values, forecast the population for future years, and visualize
the population growth trend.



    
