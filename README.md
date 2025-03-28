# Date Class in Java

## Overview
This project implements a `Date` class in Java that supports date validation, comparison, date updates, weekday calculation, and computing differences between two dates.

## Features
- Validate date format
- Compare and sort dates
- Update an existing date
- Get the weekday for a given date
- Compute the difference in days between two dates
- Print the date in a readable format

## Class: `Date`

### `Date(int day, int month, int year)`
**Description:**
Constructs a `Date` object with the specified day, month, and year.

**Parameters:**
- `day` (int): The day of the month.
- `month` (int): The month of the year (1-12).
- `year` (int): The year.

**Throws:**
- Prints "Invalid date" if the date is not valid.

---

### `boolean isValidDate(int day, int month, int year)`
**Description:**
Checks if the given date is valid.

**Returns:**
- `true` if valid, `false` otherwise.

---

### `void updateDate(int day, int month, int year)`
**Description:**
Updates the `Date` object with new values if the date is valid.

**Throws:**
- Prints "Invalid date" if the new date is not valid.

---

### `String getDayOfWeek()`
**Description:**
Determines the day of the week for the current date using Zeller's Congruence formula.

**Returns:**
- The weekday name (`Monday`, `Tuesday`, etc.).

---

### `void printDate()`
**Description:**
Prints the date in a readable format: `Month day, year` (e.g., `January 1, 2023`).

---

### `int compareTo(Date other)`
**Description:**
Compares this date with another date for sorting.

**Returns:**
- A negative number if this date is earlier, zero if equal, or a positive number if later.

---

### `int toDays()`
**Description:**
Converts the date to the total number of days since year 0.

**Returns:**
- The total number of days.

---

### `int calculateDifference(Date otherDate)`
**Description:**
Calculates the absolute difference in days between two dates.

**Returns:**
- The number of days between the two dates.

---

### `int countLeapYears(int year)`
**Description:**
Counts the number of leap years from year 0 to the given year.

**Returns:**
- The count of leap years.

---

### `boolean isLeapYear(int year)`
**Description:**
Checks if the given year is a leap year.

**Returns:**
- `true` if it is a leap year, `false` otherwise.

---

## Class: `Main`
### `public static void main(String[] args)`
**Description:**
Demonstrates the usage of the `Date` class with sorting, date difference calculation, and updating a date.

**Example Usage:**
```java
List<Date> dates = new ArrayList<>();
dates.add(new Date(15, 5, 2022));
dates.add(new Date(10, 3, 2021));
dates.add(new Date(1, 1, 2023));

Collections.sort(dates);
for (Date d : dates) {
    d.printDate();
}

Date d1 = new Date(1, 1, 2020);
Date d2 = new Date(1, 1, 2024);
System.out.println("Difference: " + d1.calculateDifference(d2) + " days");

Date d3 = new Date(1, 1, 2020);
d3.updateDate(12, 3, 2023);
d3.printDate();
d3.updateDate(12, 13, 2023); // Invalid date
```

## Notes
- Uses Zeller's Congruence to determine the weekday.
- Implements `Comparable<Date>` for sorting.
- Uses `updateDate()` to modify date values dynamically.
- Leap years are correctly handled.

## Author
- Developed as a Java learning exercise for date manipulation and comparison.

