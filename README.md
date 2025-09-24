# Surroundings

A multi-disciplinary creative technology project that combines **generative music composition**, **spatial light installations**, and **live coding** to create immersive audiovisual experiences.


## Overview

Surroundings is a comprehensive creative ecosystem that bridges algorithmic composition, spatial audio, wireless lighting, and real-time visuals into unified audiovisual experiences for concerts, installations, and immersive art pieces.

## Project Components

### 🎵 [ORCΛ (Orca)](./Orca/) - Livecoding Sequencer
- **Esoteric programming language** for creating procedural music sequencers
- Grid-based visual interface where each letter of the alphabet is an operation
- Generates MIDI, OSC, and UDP data to control external applications
- Contains multiple `.orca` files with compositional patterns focusing on **8-channel surround sound**

**Key Files:**
- `surrounding Project/orca/Surround.orca` - Main surround sound composition
- `surrounding Project/orca/Surroundings_Functions.orca` - Reusable functions
- `surrounding Project/orca/CrystalCreek/` - Extended composition suite

### 🌐 [Λioi (Aioi)](./aioi/) - OSC Message Router
- **Electron-based companion app** for Orca
- Handles **complex OSC messages** with multiple parameters and routing
- Bridges Orca's simple output to complex audio/visual software
- GUI for dynamic OSC destination configuration

**Features:**
- Multi-host OSC routing
- Complex parameter handling (floats, strings, integers)
- Real-time message testing and monitoring

### 💡 [Spore](./Spore/) - Wireless LED System
- **Hardware/software platform** for spatial light installations
- Softball-sized, WiFi-controlled, battery-operated RGB LED modules
- Supports 1-1000+ Spores working together wirelessly
- Uses **sACN (E1.31) protocol** for lighting control over network

**Components:**
- Custom PCB designs and firmware
- Configuration software for device management
- Integration with Lightwork computer vision mapping

### 🎨 TouchDesigner Integration
- **Real-time visual processing** project files (`spore.toe`, etc.)
- Receives data from Orca/Aioi pipeline
- Controls Spore LED network for synchronized audiovisual performances
- Multiple project versions for different compositions

### 🎧 Ableton Live Integration
- **8-channel surround sound compositions** in spatial audio format
- Multiple Live sets for different pieces:
  - "Fog" series
  - "CrystalCreek" 
  - "surrounding" variations
- MIDI programs, synthesizer presets, and audio samples
- Production-ready compositions for live performance

## System Architecture

```
ORCΛ (Composition) → Λioi (OSC Routing) → Multiple Outputs:
                                         ├── Ableton Live (Audio)
                                         ├── TouchDesigner (Visuals)
                                         └── Spore Network (Lighting)
```

## Getting Started

### Prerequisites
- Node.js 8+ (for Aioi)
- Arduino IDE (for Spore firmware)
- Ableton Live (for audio compositions)
- TouchDesigner (for visual processing)
- Network router with multicast support (for Spore system)

### Quick Setup

1. **Install ORCΛ:**
   ```bash
   cd Orca/desktop/
   npm install
   npm start
   ```

2. **Setup Λioi:**
   ```bash
   cd aioi/desktop/
   npm install
   npm run start
   ```

3. **Configure Spore Network:**
   ```bash
   cd Spore/configApp/
   npm install
   npm start
   ```

4. **Load Compositions:**
   - Open `.orca` files in ORCΛ
   - Load corresponding `.als` files in Ableton Live
   - Open `.toe` files in TouchDesigner

## Project Structure

```
surroundings/
├── Orca/                    # Livecoding sequencer
├── aioi/                    # OSC message router
├── Spore/                   # Wireless LED system
├── surrounding Project/     # Main compositions
│   ├── 8D/                 # 8-channel audio projects
│   ├── orca/               # Orca composition files
│   ├── Samples/            # Audio samples
│   └── Presets/            # Synthesizer presets
├── MIDI Programs/          # Synthesizer configurations
├── spore.toe              # TouchDesigner main project
└── Backup/                # Project backups
```

## Compositions

### Featured Works
- **Fog Series** - Ambient spatial compositions with evolving textures
- **CrystalCreek** - Complex algorithmic patterns with crystalline structures  
- **Surrounding** - Core spatial audio pieces exploring immersive sound design

Each composition integrates:
- Algorithmic music generation (Orca)
- 8-channel spatial audio (Ableton Live)
- Synchronized lighting (Spore network)
- Real-time visuals (TouchDesigner)

## Performance Setup

For live performances or installations:

1. **Audio**: 8-channel speaker array for surround sound
2. **Lighting**: Network of Spore LED modules placed throughout space
3. **Control**: Laptop running Orca → Aioi → Ableton/TouchDesigner
4. **Network**: Dedicated WiFi network for Spore communication

## Technical Requirements

### Hardware
- 8-channel audio interface
- Spore LED modules (1-100+)
- Network router with multicast support
- Computer capable of running multiple audio/visual applications

### Software
- ORCΛ (included)
- Λioi (included) 
- Ableton Live 10+
- TouchDesigner
- Node.js runtime

## Contributing

This project represents an integrated creative ecosystem. When contributing:
- Test changes across all components
- Maintain synchronization between audio, visual, and lighting elements
- Document any new compositional patterns or techniques

## License

Individual components maintain their respective licenses:
- ORCΛ: MIT License
- Λioi: Check component license
- Spore: Check component license

## Credits

Developed for immersive audiovisual performances combining algorithmic composition, spatial audio, and interactive lighting installations.

---

*For detailed documentation on individual components, see their respective README files in each subdirectory.*
