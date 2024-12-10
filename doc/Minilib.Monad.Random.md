# `module Minilib.Monad.Random`

Random Number Generator Monad

# Types and aliases

# Traits and aliases

## `namespace Minilib.Monad.Random`

### `trait [m : *->*] m : MonadRandomIF`

A trait for a monad that generates random numbers every time.

#### method `random_U64 : m Std::U64`

`random_U64` generates a random integer of U64.

#### method `random_bytes : Std::I64 -> m (Std::Array Std::U8)`

`random_bytes` generates random bytes of specified size.

# Trait implementations

### `impl [m : Std::Monad, rng : Minilib.Trait.Rng::Rng] Minilib.Monad.State::StateT rng m : Minilib.Monad.Random::MonadRandomIF`

# Values

## `namespace Minilib.Monad.Random`

### `random_U16 : [m : Minilib.Monad.Random::MonadRandom] m Std::U16`

`random_U16` generates a random integer of U8.

### `random_U32 : [m : Minilib.Monad.Random::MonadRandom] m Std::U32`

`random_U32` generates a random integer of U32.

### `random_U8 : [m : Minilib.Monad.Random::MonadRandom] m Std::U8`

`random_U8` generates a random integer of U8.

### `random_array : [m : Std::Monad] Std::I64 -> m a -> m (Std::Array a)`

`random_array(size, random)` generates a random array of specified size
by performing `random` repeatedly.

## `namespace Minilib.Monad.Random::MonadRandomIF`

### `random_U64 : [m : Minilib.Monad.Random::MonadRandomIF] m Std::U64`

`random_U64` generates a random integer of U64.

### `random_bytes : [m : Minilib.Monad.Random::MonadRandomIF] Std::I64 -> m (Std::Array Std::U8)`

`random_bytes` generates random bytes of specified size.