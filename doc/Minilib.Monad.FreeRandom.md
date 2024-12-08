# `module Minilib.Monad.FreeRandom`

# Types and aliases

## `namespace Minilib.Monad.FreeRandom`

### `type FreeRandom a = box union { ...variants... }`

Free Random Monad.

This type may be used in a situation such as polymorphic types cannot be used,
for example an interface of an API.

#### variant `fr_pure : a`

#### variant `fr_u64 : Std::U64 -> Minilib.Monad.FreeRandom::FreeRandom a`

#### variant `fr_bytes : (Std::I64, Std::Array Std::U8 -> Minilib.Monad.FreeRandom::FreeRandom a)`

# Traits and aliases

# Trait implementations

### `impl Minilib.Monad.FreeRandom::FreeRandom : Minilib.Monad.Random::MonadRandomIF`

### `impl Minilib.Monad.FreeRandom::FreeRandom : Std::Functor`

### `impl Minilib.Monad.FreeRandom::FreeRandom : Std::Monad`

# Values

## `namespace Minilib.Monad.FreeRandom::FreeRandom`

### `as_fr_bytes : Minilib.Monad.FreeRandom::FreeRandom a -> (Std::I64, Std::Array Std::U8 -> Minilib.Monad.FreeRandom::FreeRandom a)`

Unwraps a union value of `FreeRandom` as the variant `fr_bytes`.
If the value is not the variant `fr_bytes`, this function aborts the program.

### `as_fr_pure : Minilib.Monad.FreeRandom::FreeRandom a -> a`

Unwraps a union value of `FreeRandom` as the variant `fr_pure`.
If the value is not the variant `fr_pure`, this function aborts the program.

### `as_fr_u64 : Minilib.Monad.FreeRandom::FreeRandom a -> Std::U64 -> Minilib.Monad.FreeRandom::FreeRandom a`

Unwraps a union value of `FreeRandom` as the variant `fr_u64`.
If the value is not the variant `fr_u64`, this function aborts the program.

### `fr_bytes : (Std::I64, Std::Array Std::U8 -> Minilib.Monad.FreeRandom::FreeRandom a) -> Minilib.Monad.FreeRandom::FreeRandom a`

Constructs a value of union `FreeRandom` taking the variant `fr_bytes`.

### `fr_pure : a -> Minilib.Monad.FreeRandom::FreeRandom a`

Constructs a value of union `FreeRandom` taking the variant `fr_pure`.

### `fr_u64 : (Std::U64 -> Minilib.Monad.FreeRandom::FreeRandom a) -> Minilib.Monad.FreeRandom::FreeRandom a`

Constructs a value of union `FreeRandom` taking the variant `fr_u64`.

### `interpret : [m : Minilib.Monad.Random::MonadRandom] Minilib.Monad.FreeRandom::FreeRandom a -> m a`

### `is_fr_bytes : Minilib.Monad.FreeRandom::FreeRandom a -> Std::Bool`

Checks if a union value of `FreeRandom` is the variant `fr_bytes`.

### `is_fr_pure : Minilib.Monad.FreeRandom::FreeRandom a -> Std::Bool`

Checks if a union value of `FreeRandom` is the variant `fr_pure`.

### `is_fr_u64 : Minilib.Monad.FreeRandom::FreeRandom a -> Std::Bool`

Checks if a union value of `FreeRandom` is the variant `fr_u64`.

### `mod_fr_bytes : ((Std::I64, Std::Array Std::U8 -> Minilib.Monad.FreeRandom::FreeRandom a) -> (Std::I64, Std::Array Std::U8 -> Minilib.Monad.FreeRandom::FreeRandom a)) -> Minilib.Monad.FreeRandom::FreeRandom a -> Minilib.Monad.FreeRandom::FreeRandom a`

Updates a value of union `FreeRandom` by applying a function if it is the variant `fr_bytes`, or doing nothing otherwise.

### `mod_fr_pure : (a -> a) -> Minilib.Monad.FreeRandom::FreeRandom a -> Minilib.Monad.FreeRandom::FreeRandom a`

Updates a value of union `FreeRandom` by applying a function if it is the variant `fr_pure`, or doing nothing otherwise.

### `mod_fr_u64 : ((Std::U64 -> Minilib.Monad.FreeRandom::FreeRandom a) -> Std::U64 -> Minilib.Monad.FreeRandom::FreeRandom a) -> Minilib.Monad.FreeRandom::FreeRandom a -> Minilib.Monad.FreeRandom::FreeRandom a`

Updates a value of union `FreeRandom` by applying a function if it is the variant `fr_u64`, or doing nothing otherwise.