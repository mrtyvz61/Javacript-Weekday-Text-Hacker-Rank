## Javascript(Basic) - Weekday-Text-Hacker-Rank 

Implement the function weekdayText such that:

- It takes a single argument weekdays, which is an array of strings.
- It returns a new function that called getText that takes a single integer argument, number, and does the following;
-- It returns the value from the weekdays array at that 0-based index number
-- If number is out of range, the function throws an Error object with the message of invalid weekday number
- for example calling weekdayText['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'] must return a function getText such that calling getText(6) return 'Sun'. 'Sun' is at index 6 in the array.

 ```js
   function weekdayText(weekdays) {
      return function getText(target) {
        return weekdays[target] || (function() {
          throw new Error(`Invalid weekday numer ${target}`)
        }());
      }
    }

    daysInWeek = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'];
    
    getText = weekdayText(daysInWeek)
    
    console.log(getText(5))

