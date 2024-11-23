<p>
  <a href="">
    <img alt="npm version" src="https://badgen.net/github/commits/ahsanu123/iwaki/">
  </a>
  <a href="">
    <img alt="npm" src="https://badgen.net/github/contributors/ahsanu123/iwaki/">
  </a>
  <a href="">
    <img alt="npm" src="https://badgen.net/github/branches/ahsanu123/iwaki/">
  </a>
  <a href="https://github.com/ahsanu123/iwaki/blob/main/LICENSE">
    <img alt="licence" src="https://badgen.net/github/license/ahsanu123/iwaki/">
  </a>
</p>

<p align="center">
  <img src="./doc/iwaki_logo.svg" style="width: 400px;  "/> <br/>
   Automated Fish Cultivation
</p>


# 🐟 IWAKI - Automated Fish Cultivation

Initial System Design 

```mermaid
---
title: Block Diagram of System
---
classDiagram

note for DCMotor "this will use for spreading food"
note for Board "Use ESP32 to send data into server"
note for Spreader "Mechanic Spreader"

PowerSupply <|-- Board 
Board <|-- DCMotor
Board <|-- TempSensor
Board <|-- ESP32
Board <|-- SalinityAndPH
Board <|-- SSR
Board <|-- IOExpantion

IOExpantion <|-- SolenoidValve

SSR <|-- Pump


Spreader <|-- Board
Hopper <|-- Spreader

Server <|-- Board
Server <|-- Mobile

namespace Electronic {
class IOExpantion
class SalinityAndPH
class Board
class DCMotor
class ESP32
class TempSensor
class SSR
}

namespace Feeder{
class Spreader
class Hopper
}

namespace App{
class Mobile
}

namespace Backend{
class Server
}

```

## 🌳 Logs
- create initial system design, 23 november 2024 at ⏰ 14:26

## 🎈 Reference 
![image](https://github.com/user-attachments/assets/c64e82f2-2251-4dd0-a8bc-d3aaa5ec4479)
- [A Guide to Recirculation Aquaculture](https://openknowledge.fao.org/server/api/core/bitstreams/a0297773-095a-4ae7-9a89-5a3bfb48abc7/content)
- [a freecad manual](https://www.freecad.org/manual/a-freecad-manual.pdf)
