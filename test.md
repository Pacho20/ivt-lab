# Test cases for GT4500 class fireTorpedo method

## Specification

Tries to fire the torpedo stores of the ship.

@param firingMode how many torpedo bays to fire

 SINGLE: fires only one of the bays.
 - For the first time the primary store is fired.
 - To give some cooling time to the torpedo stores, torpedo stores are fired alternating.
 - But if the store next in line is empty, the ship tries to fire the other store.
 - If the fired store reports a failure, the ship does not try to fire the other one.

ALL:	tries to fire both of the torpedo stores.

@return whether at least one torpedo was fired successfully

## Tests

### 1

Test SINGLE mode first time fire. For the first time should fire from primary store

### 2

Test SINGLE mode alternating fire when neither store is empty.

### 3

Test SINGLE mode alternating fire when one store is empty.

### 4

Test SINGLE mode fire when both stores are empty.

### 5

Test ALL mode fire when neither store is empty.