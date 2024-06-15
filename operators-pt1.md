# Bitwise Operator Cheatsheet

| Operator | Name                    | Description                                                                 | Example                          | Explanation                                                                 |
|----------|-------------------------|-----------------------------------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------|
| `&`      | AND                     | Performs a bitwise AND operation. Only the bits that are 1 in both operands | `5 & 3` results in `1`           | `0101 & 0011 = 0001`                                                        |
| `|`      | OR                      | Performs a bitwise OR operation. The bits that are 1 in either operand      | `5 \| 3` results in `7`          | `0101 \| 0011 = 0111`                                                       |
| `^`      | XOR                     | Performs a bitwise XOR operation. The bits that are 1 in one operand but not both | `5 ^ 3` results in `6`           | `0101 ^ 0011 = 0110`                                                        |
| `~`      | NOT                     | Performs a bitwise NOT operation. Inverts all the bits                      | `~5` results in `-6`             | `~0101 = 1010` (two's complement)                                           |
| `<<`     | Left Shift              | Shifts the bits of the first operand left by the number of positions specified by the second operand | `5 << 1` results in `10`         | `0101 << 1 = 1010`                                                          |
| `>>`     | Right Shift             | Shifts the bits of the first operand right by the number of positions specified by the second operand | `5 >> 1` results in `2`          | `0101 >> 1 = 0010`                                                          |
| `>>>`    | Unsigned Right Shift    | Shifts the bits of the first operand right by the number of positions specified by the second operand, without sign extension (JavaScript only) | `-5 >>> 1` results in `2147483645` | `-5` is `111...11011`, shifted becomes `0111...11101`                      |
| `&=`     | AND Assignment          | Performs a bitwise AND operation and assigns the result to the variable     | `a &= b`                         | `a = a & b`                                                                 |
| `|=`     | OR Assignment           | Performs a bitwise OR operation and assigns the result to the variable      | `a \|= b`                        | `a = a \| b`                                                                |
| `^=`     | XOR Assignment          | Performs a bitwise XOR operation and assigns the result to the variable     | `a ^= b`                         | `a = a ^ b`                                                                 |
| `<<=`    | Left Shift Assignment   | Performs a left shift and assigns the result to the variable                | `a <<= 1`                        | `a = a << 1`                                                                |
| `>>=`    | Right Shift Assignment  | Performs a right shift and assigns the result to the variable               | `a >>= 1`                        | `a = a >> 1`                                                                |
| `>>>=`   | Unsigned Right Shift Assignment | Performs an unsigned right shift and assigns the result to the variable (JavaScript only) | `a >>>= 1`                       | `a = a >>> 1`                                                               |
| `&^`     | AND NOT (Go only)       | Clears the bits in the first operand where the corresponding bit in the second operand is 1 | `5 &^ 3` results in `4`          | `0101 &^ 0011 = 0100`                                                       |
| `<<>`    | Rotate Left (custom)    | Rotates the bits of the operand to the left by the specified number of positions (not standard in most languages, can be implemented using shifts and ORs) | `rotate_left(5, 1)` results in `10` | `0101` rotated left by 1 is `1010`                                           |
| `<>`     | Rotate Right (custom)   | Rotates the bits of the operand to the right by the specified number of positions (not standard in most languages, can be implemented using shifts and ORs) | `rotate_right(5, 1)` results in `10` | `0101` rotated right by 1 is `1010`                                          |
| `<<<`    | Arithmetic Left Shift   | Same as the logical left shift `<<` but preserves the sign bit for signed numbers | `-4 <<< 1` results in `-8`        | Arithmetic shift left of `111...1100` by 1 results in `111...1000`          |
| `>>`     | Arithmetic Right Shift  | Shifts the bits of the operand to the right, preserving the sign bit         | `-4 >> 1` results in `-2`         | Arithmetic shift right of `111...1100` by 1 results in `111...1110`         |

## Examples and Explanations

### AND Operator (`&`)
- **Operation**: `5 & 3`
- **Binary**: `0101 & 0011`
- **Result**: `0001` (1)

### OR Operator (`|`)
- **Operation**: `5 | 3`
- **Binary**: `0101 | 0011`
- **Result**: `0111` (7)

### XOR Operator (`^`)
- **Operation**: `5 ^ 3`
- **Binary**: `0101 ^ 0011`
- **Result**: `0110` (6)

### NOT Operator (`~`)
- **Operation**: `~5`
- **Binary**: `~0101`
- **Result**: `1010` (-6 in two's complement)

### Left Shift Operator (`<<`)
- **Operation**: `5 << 1`
- **Binary**: `0101 << 1`
- **Result**: `1010` (10)

### Right Shift Operator (`>>`)
- **Operation**: `5 >> 1`
- **Binary**: `0101 >> 1`
- **Result**: `0010` (2)

### Unsigned Right Shift Operator (`>>>`)
- **Operation**: `-5 >>> 1`
- **Binary**: `111...11011 >>> 1`
- **Result**: `0111...11101` (2147483645)

### AND Assignment Operator (`&=`)
- **Operation**: `a &= b`
- **Explanation**: `a = a & b`

### OR Assignment Operator (`|=`)
- **Operation**: `a |= b`
- **Explanation**: `a = a | b`

### XOR Assignment Operator (`^=`)
- **Operation**: `a ^= b`
- **Explanation**: `a = a ^ b`

### Left Shift Assignment Operator (`<<=`)
- **Operation**: `a <<= 1`
- **Explanation**: `a = a << 1`

### Right Shift Assignment Operator (`>>=`)
- **Operation**: `a >>= 1`
- **Explanation**: `a = a >> 1`

### Unsigned Right Shift Assignment Operator (`>>>=`)
- **Operation**: `a >>>= 1`
- **Explanation**: `a = a >>> 1`

### AND NOT Operator (`&^`) (Go only)
- **Operation**: `5 &^ 3`
- **Binary**: `0101 &^ 0011`
- **Result**: `0100` (4)
