# GDScript

*- programming language for Godot.*

## Functions

### Initialization

```gdscript
## Nodes are initialized by top-down approach.
## +-----------------------------------------------+
## |NODE           _init()  _enter_tree()  _ready()|
## |-----------------------------------------------|
## |parent         (01)     (08)           (21)    |
## |  child_1       (02)     (09)           (17)   |
## |    child_1_a    (03)     (10)           (15)  |
## |    child_1_b    (04)     (11)           (16)  |
## |  child_2       (05)     (12)           (20)   |
## |    child_2_a    (06)     (13)           (18)  |
## |    child_2_b    (07)     (14)           (19)  |
## +-----------------------------------------------+

## Called on start.
func _init() -> void:
	pass

## Called on start after _init().
func _enter_tree() -> void:
	pass

## Called on start after _init() and _enter_tree().
func _ready() -> void:
	pass
```

### Continuation

```gdscript
## Called every frame (FPS/s).
## - delta = time in seconds between refreshes.
func _process(delta: float) -> void:
	pass

## Called at fixed rate (60/s by default).
## - delta = time in seconds between refreshes.
func _physics_process(delta: float) -> void:
	pass
```

---

## Comments

- Comment: anything from `#` to EOL is comment:
    ```gdscript
    # Simple comment.
    ... # Another comment.
    ```
- Code regions:
    ```gdscript
    #region
    ...
    #endregion

    #region <regio
    ...
    #endregion
    ```

## Variables

```gdscript
## Variable.
var <name> := <value>

## Unchangeable variable.
const <name> := <value>

```

## Annotations

```gdscript
## Export variable to GUI (cannot be used for constants).
@export var <name> := <value>

```

https://docs.godotengine.org/en/stable/classes/class_%40gdscript.html#annotations

## User Input
