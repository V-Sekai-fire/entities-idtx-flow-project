# idtx-flow-project

Headless test project for the idtx-flow GDExtension.


This is a minimal Godot 4.5+ project for exercising the extension
without an editor. Build the extension in `idtx-flow` (`scons`), which
installs into `addons/IDTXFlow/`, then copy that folder here
(it is gitignored — binaries are build outputs, not sources).

    godot --headless --path . --import
    godot --headless --path . -s res://test_inbetween.gd

`inbetween_anim.usda` keys the primary 0 -> 1 -> 0 with one in-between authored
at weight 0.5. The test demands both shapes sweep to ~1 AND that they trade
places (in-between near 0 when the primary peaks): a bake without crossing-time
keys leaves the in-between flat at 0, and an in-between wrongly given the
primary's curve fails the phase check.
