### Project Setup

The first step is to add bevy game engine to the Rust project.
To do that, we need add bevy dependence to the project Cargo.toml file.
More info can be found by a  [link](https://bevyengine.org/learn/quick-start/getting-started/).

Latest version of bevy when I'm writing this post is 0.14.
```
Cargo.toml

[package]
name = "mmo"
version = "0.1.0"
edition = "2021"

[dependencies]
bevy = "0.14"
```

### Create bevy app
The next step is to create a bevy app.
Basic bevy app looks next:
```
use bevy::prelude::*;

fn main() {
    App::new()
        .add_plugins(DefaultPlugins)
        .run();
}
```
If you build an application and run it all what you will see in result is just a black window.

For my game-node I don't need ui modules like Window, Rendering, Audio, so I need to strip them.

This can be easily done in bevy, to do that `DefaultPlugins` needs to be replaced with `MinimalPlugins` also custom scheduler should be added.
An example how to that you can find by a [link](https://github.com/bevyengine/bevy/blob/main/examples/app/headless.rs).

Basic implemetaion of the bevy app without ui.
```
// This app loops forever at 60 fps
App::new()
    .add_plugins(MinimalPlugins.set(ScheduleRunnerPlugin::run_loop(Duration::from_secs_f64(1.0 / 60.0,))),)
    .run();
```
--
At this point my game-node can run a server loop (in the future I will name it as Simulation).


