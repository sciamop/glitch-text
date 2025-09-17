# 🔥 CRAZY TEXT GRASSHOPPER PYTHON SCRIPTS 🔥

This folder contains individual Grasshopper Python components for creating wild text effects. Each script is designed to be copied directly into a Python component in Grasshopper.

## 📁 Scripts Overview

### 1. `text_to_curves.py`
**Purpose**: Convert Rhino text object to curves
**Inputs**: 
- `text_object` (Rhino text object): Your text object from Rhino

**Outputs**: 
- `curves`: List of curves representing the text

### 2. `noise_warp.py`
**Purpose**: Apply Perlin-like noise warping
**Inputs**:
- `curves` (list): Input curves
- `noise_scale` (float): Noise frequency (0.01-0.5)
- `noise_strength` (float): Warp intensity (0-100)
- `seed` (int): Random seed for consistency

**Outputs**:
- `warped_curves`: Noise-distorted curves

### 3. `attractor_distort.py`
**Purpose**: Apply attractor-based distortion
**Inputs**:
- `curves` (list): Input curves
- `attractor_points` (list): List of attractor center points
- `attractor_strength` (float): Pull strength (0-100)
- `falloff_radius` (float): Influence radius (0-200)

**Outputs**:
- `distorted_curves`: Attractor-distorted curves

### 4. `voronoi_clip.py`
**Purpose**: Apply Voronoi cell-based clipping
**Inputs**:
- `curves` (list): Input curves
- `voronoi_points` (list): Voronoi cell centers
- `clip_strength` (float): Clipping intensity (0-50)

**Outputs**:
- `clipped_curves`: Voronoi-clipped curves

### 5. `thickness_variation.py`
**Purpose**: Apply variable thickness to curves
**Inputs**:
- `curves` (list): Input curves
- `base_thickness` (float): Base thickness (5-50)
- `variation_factor` (float): Variation amount (0-1)
- `noise_scale` (float): Thickness noise scale (0.01-0.5)

**Outputs**:
- `thickened_curves`: Variable thickness curves

### 6. `extrude_twist.py`
**Purpose**: Create 3D twisted extrusions
**Inputs**:
- `curves` (list): Input curves
- `extrude_height` (float): Extrusion height (20-200)
- `twist_angle` (float): Twist angle in degrees (0-360)
- `taper_factor` (float): Taper amount (0-1)
- `extrude_vector` (vector): Extrusion direction vector

**Outputs**:
- `twisted_meshes`: 3D twisted mesh objects

### 7. `master_crazy_text.py`
**Purpose**: All-in-one crazy text generator
**Inputs**:
- `curves` (list of curves): Input text curves
- `chaos_factor` (float): Overall chaos level (0-100)
- `noise_scale` (float): Noise frequency
- `noise_strength` (float): Noise distortion intensity
- `attractor_points` (list of points): Attractor centers
- `attractor_strength` (float): Attractor pull strength
- `falloff_radius` (float): Attractor influence radius
- `voronoi_points` (list): Voronoi centers
- `clip_strength` (float): Voronoi clipping intensity
- `base_thickness` (float): Base thickness for variation
- `variation_factor` (float): Thickness variation amount
- `thickness_noise_scale` (float): Thickness noise scale
- `extrude_height` (float): 3D height
- `twist_angle` (float): Twist amount
- `taper_factor` (float): Taper amount
- `extrude_vector` (vector): Extrusion direction vector
- `is_extrude` (bool): Whether to create 3D extrusion

**Outputs**:
- `final_curves`: Final distorted curves
- `final_meshes`: Final 3D meshes

## 🚀 How to Use

### Method 1: Individual Components
1. **Create text in Rhino** first
2. **Add Python Component** to your Grasshopper canvas
3. **Copy script content** from any `.py` file
4. **Paste into Python component**
5. **Connect Rhino text object** to input
6. **Set other parameters** as specified
7. **Connect outputs** to other components

### Method 2: Master Component
1. **Create text curves** using Text Curves component or text_to_curves.py
2. **Use `master_crazy_text.py`** for all effects at once
3. **Connect curves** and other inputs
4. **Get both curves and meshes** as outputs
5. **Adjust `chaos_factor`** to control overall wildness

### Method 3: Chain Effects
1. **Create text in Rhino** first
2. **Start with `text_to_curves.py`**
3. **Chain outputs** through other scripts
4. **Create custom effect combinations**
5. **Fine-tune each effect** individually

## 💡 Pro Tips

1. **Start with Master Script**: Use `master_crazy_text.py` first to see all effects
2. **Adjust Chaos Factor**: This controls overall wildness (0-100)
3. **Use Extreme Values**: Don't be afraid to push parameters to limits
4. **Chain Effects**: Combine multiple scripts for maximum chaos
5. **Preview Often**: Use Grasshopper's preview to see results in real-time

## 🎯 Parameter Ranges

- **Chaos Factor**: 0-100 (higher = more wild)
- **Noise Scale**: 0.01-0.5 (lower = smoother)
- **Noise Strength**: 0-100 (higher = more distortion)
- **Attractor Strength**: 0-100 (higher = stronger pull)
- **Falloff Radius**: 0-200 (larger = wider influence)
- **Clip Strength**: 0-50 (higher = more clipping)
- **Base Thickness**: 5-50 (higher = thicker)
- **Extrude Height**: 20-200 (higher = taller 3D)
- **Twist Angle**: 0-360 (full rotation)

## 🔧 Troubleshooting

**"Script not working"**
- Check that all inputs are connected
- Verify parameter types match (str, float, point, list)
- Make sure Python component is enabled

**"Performance is slow"**
- Reduce point count in scripts (change 100 to 50)
- Lower extrude height steps (change 20 to 10)
- Simplify voronoi point count

**"Results look weird"**
- Try different parameter ranges
- Check that attractor and voronoi points are reasonable
- Verify font name is valid

## 🎨 Creative Combinations

- **Wave + Noise**: Organic, flowing text
- **Attractor + Voronoi**: Geometric, structured chaos
- **Thickness + Extrude**: 3D variable-width text
- **All Effects**: Maximum visual chaos

---

**Remember**: These scripts are designed to create wild, chaotic text effects. Don't be afraid to experiment with extreme values - that's where the magic happens! 🔥
