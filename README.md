# entities-idtx-flow-project

A Godot test project that checks the idtx-flow extension's bake of blend-shape in-betweens.

## What it is for

The test plays a USD animation that keys a primary blend shape with one in-between, and fails unless both shapes sweep fully and trade places in phase.

## Run

Build [idtx-flow](https://github.com/V-Sekai-fire/idtx-flow) and copy the addon it installs into this project, then:

    godot --path . --import
    godot --path . --script res://test_inbetween.gd

## Licence

The licence is not stated.
