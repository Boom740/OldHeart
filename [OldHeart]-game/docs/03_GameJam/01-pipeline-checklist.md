---
type: jam-pipeline
version: 0.1
date: [21/07/26]
team: [OldHeart]
---
# Pipeline Function Checklist — [ชื่อเกม]

> เกมทุกแนวต้องมี pipeline ขั้นต่ำนี้ก่อนถึงจะเรียกว่า "เล่นได้" — เติมชื่อผู้รับผิดชอบและติ๊กสถานะระหว่างลงมือทำจริง เพิ่มแถวได้ถ้าเกมของทีมต้องการ module อื่น

## Must-Have (ต้องมีก่อน Hour 24 — Playable Build)

| Module (ตาม MonoGame Game Loop)             | หน้าที่                                                            | สถานะ     | ผู้รับผิดชอบ         |
| ---------------------------------------------- | ------------------------------------------------------------------------- | -------------- | -------------------------------- |
| `GameStateManager`                           | สลับ state (Menu / Playing / Pause / GameOver)                        | 🔲 Not Started | [วงศ์วรรธน์ 682110139] |
| `InputManager`                               | รับ input keyboard/gamepad แบบรวมศูนย์                      | 🔲 Not Started | [วงศ์วรรธน์ 682110139] |
| Core `Update()` logic ของกลไกหลัก | logic ของ core mechanic 1 อย่างที่เป็นหัวใจเกม     | 🔲 Not Started | [วงศ์วรรธน์ 682110139] |
| Collision / interaction พื้นฐาน         | ตรวจชน/ตรวจ trigger ระหว่าง entity                       | 🔲 Not Started | [วงศ์วรรธน์ 682110139] |
| `SpriteBatch` render + camera/viewport       | วาดผ่าน `GraphicsDevice.Viewport` (ห้าม hardcode resolution) | 🔲 Not Started | [ณัฏฐกิตติ์ 682110113] |
| Win / Lose condition                           | เงื่อนไขจบเกม/จบด่าน                                   | 🔲 Not Started | [ณัฏฐกิตติ์ 682110113] |
| Content pipeline (MGCB)                        | โหลด asset ผ่าน `Content.Load<T>()` เท่านั้น            | 🔲 Not Started | [ณัฏฐกิตติ์ 682110113] |
| [module เพิ่มเติมของเกมนี้]  |                                                                           | 🔲 Not Started | [ชื่อ]                       |

## Nice-to-Have (ทำถ้าเหลือเวลา — Hour 24–34)

| Module                                | หน้าที่                           | สถานะ     | ผู้รับผิดชอบ     |
| ------------------------------------- | ---------------------------------------- | -------------- | ---------------------------- |
| `AudioManager` (SFX พื้นฐาน) | เสียงตอบสนอง action หลัก | 🔲 Not Started | [กนต์ระพี 682110104] |
| UI/HUD (score, timer)                 | แสดงสถานะระหว่างเล่น | 🔲 Not Started | [ธีรภัทร 682110121]   |
| Music / เพลงประกอบ          |                                          | 🔲 Not Started | [กนต์ระพี 682110104] |
| [feature รองอื่นๆ]            |                                          | 🔲 Not Started | [ชื่อ]                   |

## Cut-List (ตัดทิ้งก่อนถ้าเวลาไม่พอ — ห้ามเริ่มก่อน Must-Have เสร็จ)

- ❌ Save/Load
- ❌ Settings menu
- ❌ Leaderboard
- ❌ [feature อื่นที่ทีมตกลงตัดก่อน]

> เมื่อถึง **Feature Freeze (Hour 34)** ทุก module ในตารางนี้ต้องมีสถานะ ✅ Done หรือถูกย้ายไป Cut-List อย่างชัดเจน — ห้ามค้างเป็น 🔲/🟡
