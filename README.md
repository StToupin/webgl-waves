# Wavy Lines WebGL Animation

A lightweight, pixel-perfect WebGL animation creating dynamic wavy line patterns with a neon aesthetic. This project uses pure vanilla WebGL without any dependencies, making it extremely portable and efficient.

Live demo: https://sttoupin.github.io/webgl-waves/

## Features

- Smooth animated wavy line patterns
- High-DPI/Retina display support
- Soft antialiasing through mathematical approximation
- Responsive design that adapts to any screen size
- Extremely lightweight (single HTML file, ~4.5KB)
- No external dependencies

## How It Works

The animation is created with a fragment shader that:

1. Normalizes screen coordinates
2. Uses a loop to generate multiple wavy lines through trigonometric functions
3. Creates thin bright lines where mathematical functions approach zero
4. Applies different color channel divisors to create the distinctive color scheme

## Customization

You can easily customize the animation by modifying these shader parameters:

- Line density: Change the loop increment value (currently `i += 0.2`)
- Color scheme: Modify the divisors in `gl_FragColor` (currently `e / 1.6, e / 11.6, e / 1.6`)
- Line thickness: Adjust the numerator value (`0.001`) or denominator offset (`0.01`)
- Animation speed: Change the time divisor in the render loop (`/ 5000.0`)
- Wave pattern: Experiment with the trigonometric functions and their parameters

## Browser Compatibility

The animation works in all modern browsers that support WebGL:
- Chrome 9+
- Firefox 4+
- Safari 5.1+
- Edge 12+
- Opera 12+
