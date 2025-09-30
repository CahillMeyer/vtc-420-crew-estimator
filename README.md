# Crew Estimation Challenge for VTC-420

This repository contains the Python solution for the crew estimation mini-challenge, as requested in the Upwork job posting token VTC-420.

---
## Implementation

The complete implementation is contained within the `estimator.py` script.

```python
def estimate_crew(volume_cuft, bulky_count, stair_flights, long_distance):
    """Calculates the estimated crew size based on job parameters.

    This function implements the specific business rules provided in the
    VTC-420 job posting. It assumes all inputs are of the correct type.

    Args:
        volume_cuft (int): The total volume of the items in cubic feet.
        bulky_count (int): The number of bulky items.
        stair_flights (int): The number of flights of stairs.
        long_distance (bool): True if the job is a long distance.

    Returns:
        int: The final calculated crew size.
    """

    crew = 2  

    if volume_cuft > 480:
        crew += 1 

    crew += bulky_count // 2  

    if stair_flights >= 3:
        crew += 1  

    if long_distance:
        crew += 1  
      
    return crew 

output = estimate_crew(550, 3, 2, False)
print(output)
```
---
## Usage & Output
The script is designed to run the specific test case requested by the client.

### Running the Script
To execute the code, run the following command in your terminal:

``` Bash
python estimator.py
```

### Expected Output
The script will print the final calculated crew size to the console, which is 4.

```
4
```
