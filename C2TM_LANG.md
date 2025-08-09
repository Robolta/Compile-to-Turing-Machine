# Datatypes

|Type|Name|Size|Notes|
|---|---|---|---|
|u8|Unsigned Byte|1 Byte||
|u16|Unsigned Short|2 Bytes||
|u32|Unsigned Int|4 Bytes||
|u64|Unsigned Long|8 Bytes||
|uun|Unsigned UNbound|Varies|Unbound Unsigned Integer, No Size Limit|
|---|---|---|---|
|s8|Signed Byte|1 Byte||
|s16|Signed Short|2 Bytes||
|s32|Signed Int|4 Bytes||
|s64|Signed Long|8 Bytes||
|sun|Signed UNbound|Varies|Unbound Signed Integer, No Size Limit|
|---|---|---|---|
|bool|Boolean|1 Byte|Takes up 1 Byte to keep things aligned|
|char|Character|1 Byte||
|arr|Array|Varies|An array of a single type at a set length|

# Variables

Variables must be declared before use.  A declaration can also include an initial value, but this is not required until the varaible is used otherwise, at which point an initial value is required.

```
u8 x = 2;
u8 y = 2;
u8 z = x + y;
print(z);
```

The code immediately below is NOT allowed because, while the variable is declared before use, it is not given an initial value.
```
u8 some_value_idk;

print(some_value_idk);
```

The code below here IS allowed since the variable is declared, then given a value, and only then is it used.
```
u8 some_value_idk;

some_value_idk = 5;

print(some_value_idk);
```

Alternatively, this can be done with the declaration and initial value in the same line.
```
u8 some_value_idk = 5;

print(some_value_idk);
```

# Operations

|Symbol|Name|Notes|
|---|---|---|
|+|Addition||
|-|Subtraction||
|*|Multiplication||
|/|Division|Integer Division if used on Integers|
|%|Modulo||
|---|---|---|
|!|Logical NOT||
|\||Logical OR||
|&|Logical AND||
|---|---|---|
|==|Equal||
|!=|Not Equal||
|>|Greater Than||
|<|Less Than||
|>=|Greater Than or Equal To||
|<=|Less Than or Equal To||

# Conditionals

```
u8 value = 8;
char output[8];
if (value % 3 == 0) {
	output = "Fizz";
} elif (value % 5 == 0) {
	output = "Buzz";
} elif (value % 15 == 0) {
	output = "Fizzbuzz";
} else {
	output = value.to_string();
}
```

# Loops

```
for (u8 i = 0;i++;i < 100) {
	for (u8 j = 2;j++;j < i) {
		bool is_prime = true;
		if (if i % j == 0) {
			is_prime = false;
		}
	}
}
```

```
while (true) {
	print("over and ");
}
```

# Functions

```
fn factorial(u64 n) -> u64
{
	if (n == 0 | n == 1) { return n; }
	
	factorial(n - 1) * n
}
```