# EX.6 PSEUDORANDOM NUMBER GENERATION

## AIM:
Implementation of Pseudorandom Number Generation Using Standard library.

## ALGORITHM:

## ALGORITHM DESCRIPTION:
1. Set Constants
The program defines three constants:

A (1664525): The multiplier in the LCG formula.

C (101390423): The increment in the LCG formula.

M (4294967296 // 2^32): The modulus (to ensure results fit within a 32-bit unsigned integer).

Example:

These values are standard choices for LCGs and ensure uniform distribution of the generated numbers.

2. LCG Formula

The Linear Congruential Generator formula is:

      new_seed=(A×seed+C)modM

This formula generates the next random number based on the current seed.

3. User Input

The user is prompted to input two values:

seed: The initial value to start the sequence.

n: The number of random numbers to generate.

Example:

If the user enters:

Seed = 10

n = 3 (they want 3 random numbers)

4. Random Number Generation

A for loop is used to generate n random numbers:

For each iteration, the current seed is updated using the LCG formula.

The new seed is printed as the next pseudorandom number.

5. Output

The program outputs the generated pseudorandom numbers based on the user-defined seed and count.

## PROGRAM:
```
#include <stdio.h> 
//Constants for LCG 
#define A 1664525 
#define C 1013904223 
#define M 4294967296 // 2^32 
//Linear Congruential Generator function 
unsigned int lcg(unsigned int seed) { 
return (A * seed + C) % M; 
} 
int main() { 
unsigned int seed; 
int n, i; 
printf("\n      ****Simulation of Pseudorandom number 
generation****\n\n"); 
printf("Enter the seed value: "); 
scanf("%u", &seed); 
printf("Enter how many random numbers to generate: "); 
scanf("%d", &n); 
printf("Random numbers:\n"); 
for (i = 0; i < n; i++) { 
seed = lcg(seed); 
printf("%u\n", seed); 
} 
return 0; 
}
```

## SAMPLE INPUT:

Seed value: 3

No. of random numbers: 13


## SAMPLE OUTPUT:
![WhatsApp Image 2024-10-18 at 1 54 08 PM](https://github.com/user-attachments/assets/46f870a4-012b-4c7f-8f88-047ca9a8e919)

## OUTPUT:

## RESULT:
