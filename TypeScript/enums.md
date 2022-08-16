# What is Enums?
An enum is a special "class" that represents a group of constants (unchangeable variables).
Enums come in two flavors string and numeric. 

## Numeric 
By default, enums will initialize the first value to 0 and add 1 to each additional value:
```typescript
enum CardinalDirections {
  North,
  East,
  South,
  West
}
```

## String
Enums can also contain strings. This is more common than numeric enums, because of their readability and intent.

```typescript
enum CardinalDirections {
  North,
  East,
  South,
  West
}
```



## Useful link
https://www.w3schools.com/typescript/typescript_enums.php
