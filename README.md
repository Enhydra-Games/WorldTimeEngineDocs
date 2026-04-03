# Documentation
Documentation for the World Time Engine Unreal Plugin

## Table of Contents
- [Demo Level](#demo-level)
- [Blueprint](#blueprint)
  - [World Time Engine UWorldSubsystem](#world-time-engine-uworldsubsystem)
  - [Time Info](#time-info)
    - [Current Time of the Day](#current-time-of-the-day)
    - [Full Current Time](#full-current-time)
    - [Full Current Time in Seconds](#full-current-time-in-seconds)
    - [Is Paused](#is-paused)
    - [Get Time Flow Speed](#get-time-flow-speed)
  - [Time Settings](#time-settings)
    - [Flow Speed](#flow-speed)
  - [Time Manipulation](#time-manipulation)
    - [Pause Time](#pause-time)
    - [Set Time](#set-time)
    - [Add to Time](#add-to-time)
    - [Subtract from Time](#subtract-from-time)
    - [Change Time Flow Speed](#change-time-flow-speed)
  - [Time Events](#time-events)
    - [Time Modification Event](#time-modification-event)
    - [Time Flow Speed Changed Event](#time-flow-speed-changed-event)
  - [Timer Trigger](#timer-trigger)
  - [Point in Time Trigger](#point-in-time-trigger)

## Demo Level
A pre-built example level included with the plugin that lets you explore and test the time system in action before integrating it into your own project.

<img width="889" height="265" alt="image" src="https://github.com/user-attachments/assets/feb8b821-e0d3-444e-8f98-22531eb591d3" />
<img width="851" height="745" alt="image" src="https://github.com/user-attachments/assets/8a506545-ea34-43ea-bb83-40573a07896f" />
<img width="774" height="750" alt="image" src="https://github.com/user-attachments/assets/66578f93-67ad-4bb1-988f-752f795932c5" />
<img width="754" height="739" alt="image" src="https://github.com/user-attachments/assets/ee85fcd2-69c1-4d41-9c35-2e131a4bbdcb" />
<img width="1127" height="596" alt="image" src="https://github.com/user-attachments/assets/ad548c8e-388c-4fb6-ae7b-6f90b7f6e29d" />
<img width="1016" height="590" alt="image" src="https://github.com/user-attachments/assets/1481c2d3-0d0a-4f63-95bf-682144e3368b" />


## Blueprint
### World Time Engine UWorldSubsystem
The core of the plugin — a Unreal World Subsystem accessible from Blueprints that manages the global in-game time. It serves as the central hub all other time-related nodes connect to.

<img width="308" height="111" alt="image" src="https://github.com/user-attachments/assets/d9386e17-0ec4-4d27-8d9e-008efa2b343e" />

### Time Info
A collection of read-only Blueprint nodes for querying the current state of time — including the time of day, time expressed in total seconds, whether time is paused, and the current flow speed.

#### Current Time of the Day
<img width="570" height="192" alt="image" src="https://github.com/user-attachments/assets/929017c2-430b-45d5-bd67-1ccc9d5da981" />
<img width="589" height="159" alt="image" src="https://github.com/user-attachments/assets/52a77914-16e6-4cd1-b258-4f5601965025" />

#### Full Current Time
<img width="542" height="92" alt="image" src="https://github.com/user-attachments/assets/99d57988-c7c9-4615-bbc9-23ce7e6d4e12" />
<img width="579" height="166" alt="image" src="https://github.com/user-attachments/assets/7397a0b7-d5ae-4bf0-8550-652355890677" />

#### Full Current Time in Seconds
<img width="609" height="99" alt="image" src="https://github.com/user-attachments/assets/7e408cd4-19bf-44f8-bc14-18bc2b4626df" />

#### Is Paused
<img width="551" height="106" alt="image" src="https://github.com/user-attachments/assets/526e9d87-e1ea-4bfe-a88c-956c807db9a2" />

#### Get Time Flow Speed
<img width="546" height="130" alt="image" src="https://github.com/user-attachments/assets/553fa12a-6ecd-434a-91eb-7acffd129761" />

### Time settings
Nodes for configuring how time behaves in your world, such as setting the ammount of seconds/minutes/hours your world has and adjusting how fast time flows relative to real time.

<img width="628" height="212" alt="image" src="https://github.com/user-attachments/assets/ccab1dbc-b587-41ef-8177-f44394aaf4a2" />
<img width="749" height="375" alt="image" src="https://github.com/user-attachments/assets/d21786b7-2c53-4776-93f3-30d0d4ec8c6f" />

#### Flow Speed
<img width="615" height="278" alt="image" src="https://github.com/user-attachments/assets/2c040079-5514-41b5-8ebb-003ca08f29cb" />

### Time manipulation
These nodes let you actively change time at runtime — pause it, jump to a specific moment, add or subtract time, or alter how fast it passes.

#### Pause Time
<img width="661" height="155" alt="image" src="https://github.com/user-attachments/assets/c4520f6b-dee0-4e2a-8bab-f6bd45a2700c" />
<img width="613" height="150" alt="image" src="https://github.com/user-attachments/assets/c812a036-6e8e-46dc-8aae-8ca34e475799" />
<img width="592" height="168" alt="image" src="https://github.com/user-attachments/assets/71080f9f-cee6-4b28-a203-8f8f895e60f9" />

#### Set Time
<img width="571" height="239" alt="image" src="https://github.com/user-attachments/assets/d642f521-84b2-46b6-8ddb-37952e28cb1c" />

#### Add to Time
<img width="546" height="250" alt="image" src="https://github.com/user-attachments/assets/93c0f6ab-633a-4bc8-8f40-d8334651d389" />

#### Subtract from Time
<img width="554" height="217" alt="image" src="https://github.com/user-attachments/assets/f62a3d3e-c29e-4010-8e71-85076a466473" />

#### Change Time Flow Speed
<img width="557" height="181" alt="image" src="https://github.com/user-attachments/assets/ac5a6f9f-6bc5-4f43-b467-83c40ec87a02" />

### Time Events
Blueprint events that fire automatically when time changes — either when the time value is modified (set/add/subtract) or when the flow speed is altered.

#### Time modification Event
<img width="690" height="275" alt="image" src="https://github.com/user-attachments/assets/311d07ca-aafe-4c6f-b2da-1e82a8a444da" />

#### Time Flow Speed changed Event
<img width="722" height="294" alt="image" src="https://github.com/user-attachments/assets/fa957079-81c7-4053-a0e8-16758c012645" />

### Timer Trigger
A component that fires an event after a specified in-game duration has elapsed, using the plugin's time system rather than real-world time — so it respects pausing and speed changes.

<img width="693" height="371" alt="image" src="https://github.com/user-attachments/assets/662925f7-e68c-440a-8ed3-16f04e3caedd" />
<img width="595" height="199" alt="image" src="https://github.com/user-attachments/assets/d113dc35-bd06-4c9f-978b-0742994eef85" />

### Point in Time Trigger
A component that fires an event when the in-game clock reaches a specific moment in time, allowing you to schedule world events with precision.

<img width="697" height="432" alt="image" src="https://github.com/user-attachments/assets/2ab1dee5-7048-4b11-8056-374290d5615f" />
<img width="603" height="194" alt="image" src="https://github.com/user-attachments/assets/24750d1d-8c41-45b5-bb91-2f076119c53f" />


