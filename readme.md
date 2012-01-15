Open Status
=============

Version 1.0
-----------

### Introduction

__Open Status__ is a _jQuery_ plug-in which detects the current date and returns a string informing the user of that day's opening hours.

### How to use it

1. Add `jquery.openstatus.js` to your project, along with _jQuery_.
2. Create the element that will contain the text.
3. Add the following _jQuery_ to your page, to be executed on load:

    $('#ops-trigger').openStatus({
        sunday    : 'closed until Monday',
        monday    : 'open from 9am until 6pm',
        tuesday   : 'open from 9am until 6pm',
        wednesday : 'open from 10am until 4pm',
        thursday  : 'open from 9am until 6pm',
        friday    : 'open from 9am until 6pm',
        saturday  : 'open from 11am until 4pm'
    });

...where `#ops-trigger` is a selector for the element you would like to contain the generated string, and each day string is the open status of that particular day.

A demo is available in demo.html.

### Additional settings

Additional settings can be used to customise the resulting string, and should be added as parameters:

+ `string1`: The string prepended to the start of the resulting string (default `Today is <strong>`; must be a string).
+ `string2`: The string placed in the middle of the resulting string (default `</strong>; we are `; must be a string).
+ `string3`: The string appended to the end of the resulting string (default `.`; must be a string).

These strings form the result in the following way:

    string1 + DAY + string2 + OPENINGHOURS + string3

where `DAY` and `OPENINGHOURS` are generated based upon the current day.

An example of these in practice:

    $('#ops-trigger').openStatus({
        sunday    : 'closed until Monday',
        monday    : 'open from 9am until 6pm',
        tuesday   : 'open from 9am until 6pm',
        wednesday : 'open from 10am until 4pm',
        thursday  : 'open from 9am until 6pm',
        friday    : 'open from 9am until 6pm',
        saturday  : 'open from 11am until 4pm',
        string1   : 'It is: ',
        string2   : ' and we are ',
        string3   : '. See you soon!'
    });

### Author

+ Written by [Chris Cook](http://chris-cook.co.uk)
