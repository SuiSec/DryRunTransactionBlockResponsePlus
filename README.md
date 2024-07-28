# DryRunTransactionBlockResponsePlus

Redesign `DryRunTransactionBlockResponse` interface, highlight `SenderChange`.

## Install

```bash
npm install dryruntransactionblockresponseplus
```

## Usage

```typescript
import { type DryRunTransactionBlockResponsePlus, parseDryRunResult } from 'dryruntransactionblockresponseplus';
import { SuiClient } from "@mysten/sui/client";

const dataSentToFullnode = await tx.build({ client: client });
const res = await client.dryRunTransactionBlock({
  transactionBlock: dataSentToFullnode,
});
const resPlus: DryRunTransactionBlockResponsePlus = parseDryRunResult(res);

console.log(resPlus);
```

------

重新设计`DryRunTransactionBlockResponse`的数据接口，突出`sender`的交易变化。

