[UP](./index.md)

# Date Instance Properties

## Getter

### Date.prototype.getDate()
Returns the day of the month (1-31) for the specified date according to local time.

### Date.prototype.getDay()
Returns the day of the week (0-6) for the specified date according to local time.

### Date.prototype.getFullYear()
Returns the year (4 digits for 4-digit years) of the specified date according to local time.

### Date.prototype.getHours()
Returns the hour (0-23) in the specified date according to local time.

### Date.prototype.getMilliseconds()
Returns the milliseconds (0-999) in the specified date according to local time.

### Date.prototype.getMinutes()
Returns the minutes (0-59) in the specified date according to local time.

### Date.prototype.getMonth()
Returns the month (0-11) in the specified date according to local time.

### Date.prototype.getSeconds()
Returns the seconds (0-59) in the specified date according to local time.

### Date.prototype.getTime()
Returns the numeric value of the specified date as the number of milliseconds since January 1, 1970, 00:00:00 UTC (negative for prior times).

### Date.prototype.getTimezoneOffset()
Returns the time-zone offset in minutes for the current locale.

### Date.prototype.getUTCDate()
Returns the day (date) of the month (1-31) in the specified date according to universal time.

### Date.prototype.getUTCDay()
Returns the day of the week (0-6) in the specified date according to universal time.

### Date.prototype.getUTCFullYear()
Returns the year (4 digits for 4-digit years) in the specified date according to universal time.

### Date.prototype.getUTCHours()
Returns the hours (0-23) in the specified date according to universal time.

### Date.prototype.getUTCMilliseconds()
Returns the milliseconds (0-999) in the specified date according to universal time.

### Date.prototype.getUTCMinutes()
Returns the minutes (0-59) in the specified date according to universal time.

### Date.prototype.getUTCMonth()
Returns the month (0-11) in the specified date according to universal time.

### Date.prototype.getUTCSeconds()
Returns the seconds (0-59) in the specified date according to universal time.

### Date.prototype.getYear()
Returns the year (usually 2-3 digits) in the specified date according to local time. Use getFullYear() instead.

## Conversion getter

### Date.prototype.toDateString()
Returns the "date" portion of the Date as a human-readable string like 'Thu Apr 12 2018'

### Date.prototype.toISOString()
Converts a date to a string following the ISO 8601 Extended Format.

### Date.prototype.toJSON()
Returns a string representing the Date using toISOString(). Intended for use by JSON.stringify().

### Date.prototype.toGMTString()
Returns a string representing the Date based on the GMT (UT) time zone. Use toUTCString() instead.

### Date.prototype.toLocaleDateString()
Returns a string with a locality sensitive representation of the date portion of this date based on system settings.

### Date.prototype.toLocaleFormat()
Converts a date to a string, using a format string.

### Date.prototype.toLocaleString()
Returns a string with a locality sensitive representation of this date. Overrides the Object.prototype.toLocaleString() method.

### Date.prototype.toLocaleTimeString()
Returns a string with a locality sensitive representation of the time portion of this date based on system settings.

### Date.prototype.toSource()
Returns a string representing the source for an equivalent Date object; you can use this value to create a new object. Overrides the Object.prototype.toSource() method.

### Date.prototype.toString()
Returns a string representing the specified Date object. Overrides the Object.prototype.toString() method.

### Date.prototype.toTimeString()
Returns the "time" portion of the Date as a human-readable string.

### Date.prototype.toUTCString()
Converts a date to a string using the UTC timezone.

### Date.prototype.valueOf()
Returns the primitive value of a Date object. Overrides the Object.prototype.valueOf() method.
