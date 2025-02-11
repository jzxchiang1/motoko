# Nat8
8-bit unsigned integers with checked arithmetic

Most operations are available as built-in operators (e.g. `1 + 1`).

## Type `Nat8`
``` motoko no-repl
type Nat8 = Prim.Types.Nat8
```

8-bit natural numbers.

## Value `toNat`
``` motoko no-repl
let toNat : Nat8 -> Nat
```

Conversion.

## Value `fromNat`
``` motoko no-repl
let fromNat : Nat -> Nat8
```

Conversion. Traps on overflow/underflow.

## Value `fromIntWrap`
``` motoko no-repl
let fromIntWrap : Int -> Nat8
```

Conversion. Wraps on overflow/underflow.

## Function `toText`
``` motoko no-repl
func toText(x : Nat8) : Text
```

Returns the Text representation of `x`.

## Function `min`
``` motoko no-repl
func min(x : Nat8, y : Nat8) : Nat8
```

Returns the minimum of `x` and `y`.

## Function `max`
``` motoko no-repl
func max(x : Nat8, y : Nat8) : Nat8
```

Returns the maximum of `x` and `y`.

## Function `equal`
``` motoko no-repl
func equal(x : Nat8, y : Nat8) : Bool
```

Returns `x == y`.

## Function `notEqual`
``` motoko no-repl
func notEqual(x : Nat8, y : Nat8) : Bool
```

Returns `x != y`.

## Function `less`
``` motoko no-repl
func less(x : Nat8, y : Nat8) : Bool
```

Returns `x < y`.

## Function `lessOrEqual`
``` motoko no-repl
func lessOrEqual(x : Nat8, y : Nat8) : Bool
```

Returns `x <= y`.

## Function `greater`
``` motoko no-repl
func greater(x : Nat8, y : Nat8) : Bool
```

Returns `x > y`.

## Function `greaterOrEqual`
``` motoko no-repl
func greaterOrEqual(x : Nat8, y : Nat8) : Bool
```

Returns `x >= y`.

## Function `compare`
``` motoko no-repl
func compare(x : Nat8, y : Nat8) : {#less; #equal; #greater}
```

Returns the order of `x` and `y`.

## Function `add`
``` motoko no-repl
func add(x : Nat8, y : Nat8) : Nat8
```

Returns the sum of `x` and `y`, `x + y`. Traps on overflow.

## Function `sub`
``` motoko no-repl
func sub(x : Nat8, y : Nat8) : Nat8
```

Returns the difference of `x` and `y`, `x - y`. Traps on underflow.

## Function `mul`
``` motoko no-repl
func mul(x : Nat8, y : Nat8) : Nat8
```

Returns the product of `x` and `y`, `x * y`. Traps on overflow.

## Function `div`
``` motoko no-repl
func div(x : Nat8, y : Nat8) : Nat8
```

Returns the division of `x by y`, `x / y`.
Traps when `y` is zero.

## Function `rem`
``` motoko no-repl
func rem(x : Nat8, y : Nat8) : Nat8
```

Returns the remainder of `x` divided by `y`, `x % y`.
Traps when `y` is zero.

## Function `pow`
``` motoko no-repl
func pow(x : Nat8, y : Nat8) : Nat8
```

Returns `x` to the power of `y`, `x ** y`. Traps on overflow.

## Function `bitnot`
``` motoko no-repl
func bitnot(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise negation of `x`, `^x`.

## Function `bitand`
``` motoko no-repl
func bitand(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise and of `x` and `y`, `x & y`.

## Function `bitor`
``` motoko no-repl
func bitor(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise or of `x` and `y`, `x \| y`.

## Function `bitxor`
``` motoko no-repl
func bitxor(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise exclusive or of `x` and `y`, `x ^ y`.

## Function `bitshiftLeft`
``` motoko no-repl
func bitshiftLeft(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise shift left of `x` by `y`, `x << y`.

## Function `bitshiftRight`
``` motoko no-repl
func bitshiftRight(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise shift right of `x` by `y`, `x >> y`.

## Function `bitrotLeft`
``` motoko no-repl
func bitrotLeft(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise rotate left of `x` by `y`, `x <<> y`.

## Function `bitrotRight`
``` motoko no-repl
func bitrotRight(x : Nat8, y : Nat8) : Nat8
```

Returns the bitwise rotate right of `x` by `y`, `x <>> y`.

## Function `bittest`
``` motoko no-repl
func bittest(x : Nat8, p : Nat) : Bool
```

Returns the value of bit `p mod 8` in `x`, `(x & 2^(p mod 8)) == 2^(p mod 8)`.

## Function `bitset`
``` motoko no-repl
func bitset(x : Nat8, p : Nat) : Nat8
```

Returns the value of setting bit `p mod 8` in `x` to `1`.

## Function `bitclear`
``` motoko no-repl
func bitclear(x : Nat8, p : Nat) : Nat8
```

Returns the value of clearing bit `p mod 8` in `x` to `0`.

## Function `bitflip`
``` motoko no-repl
func bitflip(x : Nat8, p : Nat) : Nat8
```

Returns the value of flipping bit `p mod 8` in `x`.

## Value `bitcountNonZero`
``` motoko no-repl
let bitcountNonZero : (x : Nat8) -> Nat8
```

Returns the count of non-zero bits in `x`.

## Value `bitcountLeadingZero`
``` motoko no-repl
let bitcountLeadingZero : (x : Nat8) -> Nat8
```

Returns the count of leading zero bits in `x`.

## Value `bitcountTrailingZero`
``` motoko no-repl
let bitcountTrailingZero : (x : Nat8) -> Nat8
```

Returns the count of trailing zero bits in `x`.

## Function `addWrap`
``` motoko no-repl
func addWrap(x : Nat8, y : Nat8) : Nat8
```

Returns the sum of `x` and `y`, `x +% y`. Wraps on overflow.

## Function `subWrap`
``` motoko no-repl
func subWrap(x : Nat8, y : Nat8) : Nat8
```

Returns the difference of `x` and `y`, `x -% y`. Wraps on underflow.

## Function `mulWrap`
``` motoko no-repl
func mulWrap(x : Nat8, y : Nat8) : Nat8
```

Returns the product of `x` and `y`, `x *% y`. Wraps on overflow.

## Function `powWrap`
``` motoko no-repl
func powWrap(x : Nat8, y : Nat8) : Nat8
```

Returns `x` to the power of `y`, `x **% y`. Wraps on overflow.
