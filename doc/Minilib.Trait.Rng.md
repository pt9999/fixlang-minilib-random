# `module Minilib.Trait.Rng`

# Types and aliases

# Traits and aliases

## `namespace Minilib.Trait.Rng`

### `trait rg : Rng`

A trait for Random Number Generator.

#### associated type `RngResult rg a`

#### associated type `[m : *->*] RngLift rg m a`

#### method `rng_U64 : rg -> Minilib.Trait.Rng::Rng::RngResult rg (rg, Std::U64)`

Generates a random integer of U64.

#### method `rng_bytes : Std::I64 -> rg -> Minilib.Trait.Rng::Rng::RngResult rg (rg, Std::Array Std::U8)`

Generates random bytes of specified size.

# Trait implementations

### `impl Random::Random : Minilib.Trait.Rng::Rng`

# Values

## `namespace Minilib.Trait.Rng`

### `lens_rng : [rg : Minilib.Trait.Rng::Rng, rg2 : Minilib.Trait.Rng::Rng, f : Std::Functor, Minilib.Trait.Rng::Rng::RngResult rg a = f a] ((rg -> Minilib.Functor.Pair::PairLT a f rg) -> rg2 -> Minilib.Functor.Pair::PairLT a f rg2) -> (rg -> f (rg, a)) -> rg2 -> f (rg2, a)`

Convert a `rng_xxx` function with a lens action.
Useful for implementing the `Rng` trait for a container which contains a member implementing the `Rng` trait.
For example, `rng_U64.lens_rng(act_random)` is a `rng_U64` function acting with `act_random`.
For details, see the `Container` type in `monad_random_test.fix`.
Note that this function somewhat looks like `State::lens_state_t`.

## `namespace Minilib.Trait.Rng::Rng`

### `rng_U64 : [rg : Minilib.Trait.Rng::Rng] rg -> Minilib.Trait.Rng::Rng::RngResult rg (rg, Std::U64)`

Generates a random integer of U64.

### `rng_bytes : [rg : Minilib.Trait.Rng::Rng] Std::I64 -> rg -> Minilib.Trait.Rng::Rng::RngResult rg (rg, Std::Array Std::U8)`

Generates random bytes of specified size.