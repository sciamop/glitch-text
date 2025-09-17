# Crazy Text 3D Generator 🔥

A fucking insane web-based 3D text distortion engine built with Three.js that turns boring text into animated, distorted masterpieces.

![Crazy Text 3D](https://img.shields.io/badge/Three.js-0.155.0-blue) ![Status](https://img.shields.io/badge/Status-Chaotic%20Awesome-brightgreen)

## What This Monster Does

This thing takes your text and absolutely destroys it in the most beautiful way possible:

- **3D Text Rendering** - Real font loading with proper geometry
- **Distortion Effects** - Perlin noise, attractors, Voronoi chaos
- **Animation** - Smooth, customizable motion
- **Export Capabilities** - Animated SVG and GIF frame sequences
- **Individual Letter Control** - Each character is its own 3D object
- **Polygon Management** - Smart subdivision to prevent geometry explosion

## Features That'll Blow Your Mind

### 🎨 **Visual Effects**
- **Color Modes**: Rainbow, black, white, random, position-based, noise-based
- **Background Colors**: Dark, black, white, gray, blue, red
- **Thickness Variation**: Dynamic depth changes based on noise
- **Smooth Animations**: Configurable speed and timing

### 🔧 **Distortion Controls**
- **Perlin Noise**: 3D noise distortion with scale control
- **Attractors**: Magnetic points that pull vertices (up to 30 points, max strength 1000)
- **Voronoi**: Cellular pattern distortion (up to 30 points, max strength 1000)
- **Threshold Clipping**: Hard cutoff for extreme distortions

### 📐 **Geometry Settings**
- **Resolution**: Polygon density per character (3-100)
- **2D/3D Toggle**: Render as curves or extruded 3D shapes
- **Base Depth**: Extrusion thickness for 3D mode
- **Smart Polygon Limits**: Prevents geometry explosion on curved letters (2000 max per character)

### 📝 **Text Controls**
- **Multi-line Support**: Use `/n` for line breaks
- **Line Spacing**: Vertical spacing control (-0.5 to 2.0)
- **Position Controls**: X, Y, Z positioning
- **Font Loading**: Real Three.js font with fallback system

### 📤 **Export Options**
- **Animated SVG**: 30-frame animations respecting speed settings
- **GIF Frames**: PNG sequence export for GIF creation (768px max)
- **Smart Framing**: Auto-crops to text bounds with optimal aspect ratio

## How to Use This Beast

1. **Open the HTML file** in a modern browser (fuck IE6)
2. **Type your text** in the input field
3. **Adjust the chaos** with all the sliders and controls
4. **Watch it dance** with the animation toggle
5. **Export your creation** as SVG or GIF frames

### Controls Breakdown

#### Text & Font
- **Text Input**: Your words of wisdom
- **Line Spacing**: How much space between lines
- **Resolution**: More polygons = smoother curves (but heavier)

#### Positioning
- **X/Y/Z Position**: Move your text around in 3D space

#### Distortion Effects
- **Noise Scale**: How wild the Perlin noise gets (0-2.0)
- **Attractor Count**: Number of magnetic points (1-30)
- **Attractor Strength**: How strong the pull is (0-1000)
- **Voronoi Count**: Number of cellular points (1-30)
- **Voronoi Strength**: Cellular distortion intensity (0-1000)
- **Threshold**: Hard limit for distortions

#### 3D Extrusion
- **Enable Extrusion**: Toggle between 2D curves and 3D shapes
- **Base Depth**: How thick the 3D extrusion is
- **Thickness Variation**: Dynamic depth changes

#### Visual Style
- **Color Mode**: How to color your text
- **Background**: Scene background color
- **Animation Speed**: How fast the chaos moves

## Technical Shit

### Architecture
- **Individual Letter Meshes**: Each character is a separate Three.js object
- **Polygon-Based System**: Smart subdivision based on character complexity
- **Global Coordinate System**: Proper positioning for multi-character text
- **Memory Management**: Proper disposal of old geometries

### Performance Optimizations
- **Polygon Limits**: 2000 max per character to prevent browser death
- **Smart Subdivision**: Only adds detail where needed
- **Efficient Rendering**: WebGL with fallback options
- **Export Optimization**: 3 decimal precision for file size control

### Export Details
- **SVG**: 30 frames, respects animation speed, global coordinate system
- **GIF**: PNG sequence, smart framing, 768px max width, 30 frames

## Browser Requirements

- **Modern Browser**: Chrome, Firefox, Safari, Edge
- **WebGL Support**: For 3D rendering
- **ES6 Modules**: For Three.js imports
- **File Download**: For export features

## File Structure

```
crazy_text_3d.html    # The entire fucking application
README.md            # This beautiful documentation
```

## Known Issues & Quirks

- **Font Loading**: Uses Helvetiker font with fallback system
- **Memory Usage**: High polygon counts can be heavy
- **Export Size**: SVG files can get large with complex animations
- **Browser Limits**: Very high resolution settings might crash older browsers

## Development Notes

This monstrosity evolved through:
1. **FontLoader Issues** → ES6 module imports
2. **Single Mesh** → Individual letter meshes
3. **Polygon Explosion** → Smart subdivision limits
4. **Export Problems** → Global coordinate systems
5. **Performance Issues** → Polygon management
6. **Coordinate Chaos** → Proper world space calculations

### Key Functions
- `createIndividualLetterMeshes()` - Creates separate meshes per character
- `createPolygonBasedCharacterGeometry()` - Smart polygon subdivision
- `applyDistortions()` - All the beautiful chaos
- `exportAnimatedSVG()` - SVG export with global coordinates
- `exportAnimatedGIF()` - Frame sequence export

## Contributing

Want to add more chaos? Fork it and make it even more insane. Just don't break the polygon limits or your browser will cry.

## License

Do whatever the fuck you want with it. It's art.

---

*"Sometimes you need to break text to make it beautiful."* 🎨

**Built with Three.js, Perlin noise, and way too much caffeine.**
