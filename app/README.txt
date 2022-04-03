Code to refactor
=================
1) app/Http/Controllers/BookingController.php
2) app/Repository/BookingRepository.php

Code logic looks ok but have some problem with basic logic, some formatting, and structure of the code can be improved,

Some code have been refector that most of the code lines should not be longer than 80 characters,
lines longer than that should be split into multiple subsequent lines of no more than 80 characters each.

Identity Operators(===) didn't use anywhere in the code

Type Hint is not defined in methods.

Some of the 'Strings' are repetitive so they can be replaced with CONSTANT so this code will be reusable.

In some places same variable override above values like below 
    if ($job->certified === 'both') {
        $data['job_for'][] = 'normal'; 
        $data['job_for'][] = 'certified';  // this value will override above value
    } else if ($job->certified === 'yes') {
        $data['job_for'][] = 'certified';
    } else {
        $data['job_for'][] = $job->certified;
    }
