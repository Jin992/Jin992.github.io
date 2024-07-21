## First steps

I don't have any previous experience in mmo game development or in game-dev.
All my previous experience related to the C/C++ programing and networking.

In this devlog I want to create MMORPG server from scratch.
My idea is to create scalable Map Centric game nodes.
In my opinion, this approach has a potential for future scaling.

Recently I have started to learn Rust programming language and planning to write my first mmo server on it.
Due to this, I have chose Bevy game engine as core component of my future mmo server.
I decided to choose it due to two factors:
    1. Bevy engine designed around ECS (Entity Complenent System) pattern which I think perfectly fit for implementing MMO server with huge amount of entities.
    2. Bevy engine is written on Rust.

In this project I want to use cloud native approach, deliver all services as separate docker containers and orchestrate them with kubernetes.
In my opinion, this approach should be beneficial for future scaling.

---
### Technologies:
Main progaming language: Rust
Scripting language: Lua(not sure yet)
Orchestration: kubernetes
Database: not decided yet
Game client engine: Bevy(maybe UE in the future)
