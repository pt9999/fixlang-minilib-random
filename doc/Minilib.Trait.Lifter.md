# `module Minilib.Trait.Lifter`

# Types and aliases

## `namespace Minilib.Trait.Lifter`

### `type LifterImpl from to = unbox struct { ...fields... }`

# Traits and aliases

## `namespace Minilib.Trait.Lifter`

### `trait lf : Lifter`

#### associated type `LiftTo lf`

#### associated type `LiftFrom lf`

#### method `lifter : lf`

#### method `lift_from : Minilib.Trait.Lifter::Lifter::LiftFrom lf -> lf -> Minilib.Trait.Lifter::Lifter::LiftTo lf`

# Trait implementations

### `impl [m : Std::Monad] Minilib.Trait.Lifter::LifterImpl (Minilib.Monad.Identity::Identity a) (m a) : Minilib.Trait.Lifter::Lifter`

### `impl [m : Minilib.Monad.IO::MonadIO] Minilib.Trait.Lifter::LifterImpl (Std::IO a) (m a) : Minilib.Trait.Lifter::Lifter`

### `impl [m : Minilib.Monad.IO::MonadIOFail] Minilib.Trait.Lifter::LifterImpl (Std::IO::IOFail a) (m a) : Minilib.Trait.Lifter::Lifter`

# Values

## `namespace Minilib.Trait.Lifter::Lifter`

### `lift_from : [lf : Minilib.Trait.Lifter::Lifter] Minilib.Trait.Lifter::Lifter::LiftFrom lf -> lf -> Minilib.Trait.Lifter::Lifter::LiftTo lf`

### `lifter : [lf : Minilib.Trait.Lifter::Lifter] lf`