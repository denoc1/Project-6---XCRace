# Runner Roster Analysis Project

## Objective

In this project, you will build a program that analyzes cross country race data. You will:

- Design a `Runner` class to represent each athlete
- Read runner data from a CSV file
- Write a `RunnerUtils` class with methods to analyze the data
- Display summary statistics of the runners

---

## Part 1: Runner Class

Create a `Runner` class with the following **instance variables**:

- `String name`
- `int age`
- `int grade`
- `String raceType` – should be either `"1k"`, `"5k"`, or `"10k"`
- `String time` – stored in **`hh:mm:ss`** format

Include:

- A constructor
- Getter methods for all instance variables
- A `toString()` method that returns a readable summary of the runner

You may write a private helper method like `convertToSeconds(String time)` for comparing times numerically.

---

## Part 2: Reading Data

Write code to read a CSV file containing the runner data and store each `Runner` object into an `ArrayList<Runner>`. The CSV file will be formatted as:

Name,Age,Grade,Race,Time

Example:
Mia Thomas,15,9,5k,00:23:17
Leo Zhang,17,11,10k,01:02:45

A tester file will be provided to you.


---

## Part 3: Analysis Methods

Create a separate file named **`RunnerUtils.java`**. This class should contain **only static methods** and will not need to store any data. These methods will **analyze or compute results** using an `ArrayList<Runner>` passed as a parameter.

Your `RunnerUtils` class should include the following methods (all methods must return their results instead of printing):

1. **`public static ArrayList<Runner> filterByRace(ArrayList<Runner> list, String raceType)`**  
   Returns a list of all runners who competed in the specified race type (`"1k"`, `"5k"`, or `"10k"`).

2. **`public static Runner getFastestRunnerByRace(String raceType, ArrayList<Runner> runners)`**  
   Returns the runner with the fastest time (lowest total time in seconds) in the given race.

3. **`public static String getAverageTimeByRace(String raceType, ArrayList<Runner> runners)`**  
   Returns the average time (in hh:mm:ss format) for all runners in the given race.

4. **`public static int countByGrade(ArrayList<Runner> list, int grade)`**  
   Returns the number of runners in a particular grade in all races.

5. **`public static int countByRaceType(ArrayList<Runner> list, String raceType)`**  
   Returns the number of runners in a specific race.

6. **`public static ArrayList<Runner> getNFastestRunnersByRace(String raceDistance, int n, ArrayList<Runner> runners)`**
     Returns the top n runners in a given race.

7. **`public static void getSummary(ArrayList<Runner> list)`**  
   Prints a summary in a nice readable format of:
   - Total number of runners overall
   - Number of runners in each race
   - Fastest time in each race
   - Average time of each race



---


