# base-unit-trait-single-use

The `SingleUse` unit trait: a unit type with it is destroyed when it attacks.

A unit type with this trait is spent by its attack, win or lose, and never becomes a veteran.

For example: Civ2: flag 12 (Cruise Msl, Nuclear Msl).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(SingleUse)`:

```ts
import SingleUse from '@civ-clone/base-unit-trait-single-use/SingleUse';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, SingleUse));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
