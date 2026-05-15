# Apex Basics – Short Notes

## Variables
Apex Variables are used to store data in Apex.

### Example
```apex id="rghyzv"
String name = 'Navya';
Integer age = 20;
```
# Loops
Loops are used to repeat actions multiple times.

### Example
```apex id="1bnj1k"
for(Integer i=0; i<5; i++){
    System.debug(i);
}
```

# Conditions
Conditions are used for decision-making.

### Example
```apex id="pvk8u0"
if(age >= 18){
    System.debug('Adult');
}
```

# Classes
Classes are blueprints that contain variables and methods.

### Example
```apex id="xkpr9t"
public class HelloWorld {
    public static void greet(){
        System.debug('Hello');
    }
}

# Triggers Overview
Triggers are Apex code that run automatically before or after events like insert, update, or delete on records.

### Uses
* Validate data
* Update related records
* Automate processes

### Example
```apex id="q4pq4s"
trigger ContactTrigger on Contact(before insert) {
    System.debug('Trigger Executed');
}
```
