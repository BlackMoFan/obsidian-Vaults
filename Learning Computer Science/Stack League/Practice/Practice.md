1. Overpopulation - Practice

**Background**
An alien life form abducted you and brought to their planet to solve their upcoming overpopulation problem.
The small planet has population 1000 at the beginning of a year. The population regularly increases by 2 percent per year and moreover 50 new life forms per year come to live in the planet. How many years does the planet need to see its population greater 1200 inhabitants?

**Example**
At the end of the first year there will be: 1000 + 1000 * 0.02 + 50 => 1070 inhabitants
At the end of the 2nd year there will be: 1070 + 1070 * 0.02 + 50 => 1141 inhabitants (number of inhabitants is an integer)
At the end of the 3rd year there will be: 1141 + 1141 * 0.02 + 50 => 1213
It will need 3 entire years.

**Parameters**
population, percent, additional (inhabitants coming or leaving each year), targetPopulation (population to surpass)
the function nb_year should return n number of entire years needed to get a population greater or equal to the targetPopulation.
'additional' is an integer, percent a positive or null number, 'population' and 'targetPopulation' are positive integers (> 0)

**Samples**
nb_year(1500, 5, 100, 5000) -> 15
nb_year(1500000, 2.5, 10000, 2000000) -> 10

#### Solution

```python
def nb_year(population, percent, additional, target):
  years = 0
  while population < target:
    population += (population * (percent / 100)) + additional
    years += 1
  return years
  #code here
```

```javascript
function nbYear(startingPopulation, percent, additional, targetPopulation) {
  let years = 0;
  while(startingPopulation < targetPopulation){
    startingPopulation += (startingPopulation * (percent / 100)) + additional;
    years += 1;
  }
    
  return years;
}
```

```php
function nbYear($population, $percent, $additional, $targetPopulation) {
  $years = 0;
  while($population < $targetPopulation){
    $population += ($population * ($percent / 100)) + $additional;
    $years += 1;
  }
    
  return $years;
}
```


2. Bigger Similar Digits - Practice

Create a function that accepts a positive integer and returns the next bigger integer formed using the same digits:

Example:
12 ==> 21
513 ==> 531
2017 ==> 2071

Note: If no bigger number can be composed using those digits, return -1
9 ==> -1
111 ==> -1
531 ==> -1

#### Solution

```python
def next_bigger(number):
  # Convert the integer to a string for easier manipulation
  digits = list(str(number))
  
  if len(digits) == 1:
    return -1
  # Find the first decreasing digit from right to left
  i = len(digits) - 2
  while i >= 0 and digits[i] >= digits[i + 1]:
    i -= 1
  
  if i < 0:
    # If no decreasing digit is found, it's not possible to form a bigger integer
    return -1
  
  # Find the smallest digit to the right of digits[i] that is greater than digits[i]
  j = len(digits) - 1
  while digits[j] <= digits[i]:
    j -= 1
  
  # Swap digits[i] and digits[j]
  digits[i], digits[j] = digits[j], digits[i]
  
  # Reverse the digits to the right of i
  digits[i + 1:] = reversed(digits[i + 1:])
    
  # Convert the list of digits back to an integer and return the result
  return int(''.join(digits))
```

