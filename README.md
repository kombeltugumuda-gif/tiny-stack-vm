# tiny-stack-vm

[![make.fun](https://make.fun/badge/tiny-stack-vm-01-run-20261122.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)
[![rank](https://make.fun/badge/tiny-stack-vm-01-run-20261122/kombeltugumuda-gif/tiny-stack-vm/rank.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)
[![reward](https://make.fun/badge/tiny-stack-vm-01-run-20261122/kombeltugumuda-gif/tiny-stack-vm/reward.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)

A tiny stack virtual machine in 1,331 bytes of TypeScript for the
[tiny-stack-vm-01-run-20261122](https://make.fun/bounty/tiny-stack-vm-01-run-20261122)
bounty. `main.ts` is a brotli-q11-packed full-ISA interpreter (37 opcodes);
the unpacked readable source is kept with the build record, not in this repo.

## Verification

Official scorer practice (40 instances): score 1,000,000, all 40 answered.
Differential fuzz against the kit reference VM: 0 mismatches (30,087 random
+ 87 targeted cases on the unpacked source; 587 cases through the real file
interface on the packed entry). Official `grade-local --driver process`:
every instance 1,000/1,000, L1 regrade byte-for-byte. Entry size is 1,338
bytes (1,331 + 7 path bytes), the smallest the packing could reach.
