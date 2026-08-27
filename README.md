# InterVerse AI

Versioned AI behavior, campus context, navigation knowledge, scene-generation policy, and evaluation fixtures for InterVerseSG.

This repository does **not** store API keys and does not execute Unreal actions directly. Its role is to define what the assistant is allowed to understand and request. Runtime execution remains split across `interverse-api`, `interverse-builder`, and `interverse-unreal`.

## Responsibilities

- version the InterGuide system instructions;
- maintain the campus vocabulary and navigation graph;
- define allowed action semantics;
- prevent hallucinated buildings, rooms, services, and asset types;
- define scene-generation constraints for Meta Quest;
- provide regression examples used to test future prompt/model changes.

## Runtime chain

`User -> interverse-api -> InterVerse AI policy/context -> structured command -> interverse-builder -> interverse-unreal`

## Initial scope

The MVP knows only:

- Entrance
- Reception
- North Hallway
- Classroom 101

Everything outside that scope must be treated as unknown until it is added to the campus knowledge base.
