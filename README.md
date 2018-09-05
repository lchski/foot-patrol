# FP

## Schema

### patrollers

* firstName _(string)_
* lastInitial _(string)_
* dispatcher _(boolean)_

### shifts

* time _(timestamp)_
    * Date and time of the shift. Time is the start of shift, e.g. 20:00 for B shift.
* dispatcher _(reference: patrollers)_
* patrollers _([reference: patrollers])_

### walks

* firstName _(string)_
* patrollers _([reference: patrollers])_
    * *note:* to replace with a reference to a “team” object, also attached to the shift?
* times _(object)_
    * start _(timestamp)_
    * end _(timestamp)_
