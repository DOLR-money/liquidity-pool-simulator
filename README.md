# Liquidity Pool Simulator

Attempts to simulate uniswap lp trades between ETH and an arbitrary token, with randomness.

Please look through the code before using because there are some additional actions it takes, such as rebalancing.

It is not particularly useful until you extend `LiquidityPoolSimulator` - [see Arb below](#arb).

To install:
```
pnpm i
```

To run:
```
pnpm start
```

To run w/ seed:
```
pnpm start --seed 1
```

You can pass a `config` in to `LiquidityPoolSimulator()` - see the constructor for props.

## Arb

The real magic happens when you extend LiquidityPoolSimulator with Arb in arb.js:
```
import LiquidityPoolSimulator from '../index.js';

class Arb extends LiquidityPoolSimulator {
  tryArb() {
    ...
  }
}
```

Then run:
```
pnpm arb
```

Happy trails!
