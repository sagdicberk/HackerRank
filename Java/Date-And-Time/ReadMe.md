# Problem
The Calendar class is an abstract class that provides methods for converting between a specific instant in time and a set of calendar fields such as YEAR, MONTH, DAY_OF_MONTH, HOUR, and so on, and for manipulating the calendar fields, such as getting the date of the next week.

You are given a date. You just need to write the method, , which returns the day on that date. To simplify your task, we have provided a portion of the code in the editor.

## Quick Eplanation
The findDay method calculates the day of the week for a given date (month, day, year):

* Create Calendar: A Calendar instance is created.
* Set Date: The specified date is set.
* Get Day: The day of the week is retrieved as an integer (1=Sunday).
* Return Name: The integer is used to return the corresponding day name from an array.

```java
public static String findDay(int month, int day, int year) {
        Calendar calendar = Calendar.getInstance();
        calendar.set(year,(month-1),day);
        
        int dayOfWeek = calendar.get(Calendar.DAY_OF_WEEK);
        
        String[] days = {
            "SUNDAY",    // 1
            "MONDAY",    // 2
            "TUESDAY",   // 3
            "WEDNESDAY", // 4
            "THURSDAY",  // 5
            "FRIDAY",    // 6
            "SATURDAY"   // 7
        };

        
        return days[dayOfWeek - 1];

    }
```
