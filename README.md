# Motion Amplifier

A web-based video motion amplification tool that enhances subtle movements in videos using advanced signal processing techniques. This tool is particularly useful for visualizing micro-movements that are normally invisible to the naked eye, such as breathing patterns, pulse detection, or structural vibrations.

## Features

- **Enhanced Motion Amplification Algorithm**: Uses Eulerian motion magnification with temporal filtering for high-quality results
- **Frequency Band Filtering**: Process specific frequency ranges to target different types of motion (e.g., breathing, pulse)
- **Automatic Frame Rate Detection**: Adapts processing to the actual video frame rate
- **Spatial Noise Reduction**: Applies Gaussian blur to reduce noise and improve amplification quality
- **Real-time Progress Tracking**: Visual feedback during processing with detailed status updates
- **Drag & Drop Support**: Easy file upload with validation
- **Side-by-side Comparison**: View original and amplified videos simultaneously
- **Optimized Performance**: Memory-efficient processing with automatic quality adjustments

## Usage

1. **Upload a Video**: Click "Upload a file" or drag and drop a video file (MP4, WebM, max 100MB)
2. **Adjust Parameters**:
   - **Amplification Factor**: Controls the strength of motion enhancement (5-100x, default: 15x)
   - **Frequency Range**: Target specific motion frequencies in Hz
     - Breathing: 0.2-0.8 Hz
     - Pulse: 0.8-3.0 Hz  
     - General micro-movements: 0.4-3.0 Hz
3. **Process**: Click "Process Video" and wait for the enhanced result
4. **Compare**: View the original and amplified videos side-by-side

## Technical Details

### Algorithm Overview
This implementation uses a simplified Eulerian motion magnification approach:

1. **Frame Extraction**: Extracts video frames with spatial smoothing
2. **Temporal Filtering**: Applies bandpass filtering in the frequency domain
3. **Motion Amplification**: Enhances the filtered motion signals
4. **Video Reconstruction**: Generates the output video with amplified motion

### Performance Optimizations
- Processes maximum 300 frames or 10 seconds of video for performance
- Uses VP8 codec with 2.5 Mbps bitrate for quality output
- Automatic frame rate detection and adaptation
- Memory-efficient streaming processing

### Browser Compatibility
- Modern browsers with HTML5 video support
- MediaRecorder API support required
- Canvas 2D rendering context required

## Best Results

For optimal motion amplification:
- Use videos with a **stationary camera**
- Ensure the **subject remains relatively stable**
- Choose appropriate **frequency ranges** for the type of motion
- Start with **lower amplification factors** (10-20x) and adjust as needed
- Use **good lighting** and **minimal background movement**

## Limitations

- Processing time depends on video length and complexity
- Maximum file size: 100MB
- Limited to first 10 seconds or 300 frames for performance
- Works best with stationary cameras and stable subjects
- Some artifacts may appear with very high amplification factors