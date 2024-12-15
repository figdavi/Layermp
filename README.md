# Layermp
A simple Python tool to create **key layers** activated by hotkeys.

## Features
- **Customizable profiles**: Easily create, delete, modify and transition between profiles.
- **Configurable modifier hotkeys:** Define modifier hotkeys to activate key layers based on modes
- **Layer-based key remapping:** Map keys dynamically to different actions using key layers.

## Profile
- Name
- A set of **Key Layers**

### Key Layer
- A modifier hotkey
- The modifier mode:
    - Switch: Temporarily activate a layer by holding the activate hotkey, similar to `Shift`.
    - Lock: Toggle a layer on/off by pressing the activate hotkey, similar to `CapsLock`.
- A list of key remaps:
    - source key -> destination key

#### Key Remap
- A source key (the key being remapped).
- A destination key (the key it becomes when the key layer is active).

### Example:
- Let a profile named "Meaningless" contain 1 key layer:
- Key Layer:
    - Modifier hotkey: `CapsLock`
    - Modifier mode: **Switch**
    - Key remaps: 
        - `a` -> `Delete` <br/>
        - `s` -> `F1`
        - `d` -> `up` (up arrow)

While `CapsLock` is **held**, the key layer is active (Switch mode):
```
                     _____  _____  _____ 
                    /\ Del \\  F1 \\  ↑  \ 
                    \ \_____\\_____\\_____\
                     \/_____//_____//_____/
                      /      /      / 
                  ___/_  ___/_  ___/_   
    __________   /\  a  \\  s  \\  d  \     
   \  CapsLock \ \ \_____\\_____\\_____\    
    \___________\ \/_____//_____//_____/  
```

## Installation

- Python 3.12+ needed ([Download Page](https://www.python.org/downloads/))

1. Clone the repository:
```bash
git clone https://github.com/figdavi/Layermp.git
cd layermp
```

2. Install requirements:
```bash
pip install -r requirements.txt
```

## Usage
1. Modify/Add profiles in config/profiles.json

2. In the project folder run:
```bash
python main.py
```

## Future Improvements
- Add a CLI with [Typer](https://github.com/fastapi/typer) + [Rich](https://github.com/Textualize/rich)
- Design a way to check if key names exist as keys
- Error logging
- Implement support for key to symbol remapping
- Create a pt-br README