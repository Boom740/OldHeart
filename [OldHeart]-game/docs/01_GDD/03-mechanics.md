---
type: gdd-mechanics
version: 0.1
date: [14/07/2026]
---
# Mechanic Design — [Movement / Action]

## State Diagram

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Move : กด Arrow/WASD
    Move --> Idle : ปล่อยปุ่ม
    Move --> Attack : กด Attack button
    Idle --> Attack : กด Attack button
    Attack --> Idle : Animation จบ
```

## Rules

| State  | เข้าเงื่อนไข                        | ออกเงื่อนไข | Note           |
| ------ | ----------------------------------------------- | ---------------------- | -------------- |
| Idle   | เริ่มเกม / หยุดเคลื่อนที่ | กด input ใดๆ      | Animation loop |
| Move   | กดปุ่มทิศทาง                        | ปล่อยปุ่ม     | Speed = [40]   |
| Attack | กด Left mouse                                 | ปล่อย Left mouse | Damage = [100] |
