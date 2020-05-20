# solidity string utilities.

simplify dumping data as string in solidity.

Mostly useful in testing by generating meaningful revert messages.

Currently supports `toString()` method for uint, address, bytes32.

Also provides `concat()` methods for those types, but only with 2 params.
For more params, use `abi.encodePacked()`

e.g.

```solidity
import "solidity-string-utils/StringUtils.sol";

    ...

    using StringUtils for *;

    require(condition, string(abi.encodePacked( 
        "some params:",
        " a=", a.toString(),
        " b=", b.toString()
    )));

```

