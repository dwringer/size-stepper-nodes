![size stepper usage graph](https://raw.githubusercontent.com/dwringer/size-stepper-nodes/main/size_nodes_usage.jpg)

### Installation:

To install these nodes, simply place the included `.py` files in your `invokeai/.venv/Lib/site-packages/invokeai/app/invocations/` or `invokeai/.venv/Lib/Python3.10/site-packages/invokeai/app/invocations/` folder, depending on which one exists on your system. You may also have a slightly different Python version listed. Navigate to your invokeai folder, open up .venv/Lib and you can locate the appropriate folder from there. 

### Ideal Size Stepper

Plug in your full size dimensions as well as JPPhoto's Ideal Size node's output dimensions, and get 1, 2, or 3 intermediate pairs of dimensions for upscaling based on the natural log of the image area (by default). Thus, each successive generation (from ideal size to full size) adds approximately the same percentage of new pixels to the image. Note this does not output the ideal size or full size dimensions. The 1, 2, or 3 outputs of this node are only the intermediate step sizes.

There are up to three stages which determine how many intermediate sizes to compute and output. With Tapers B and C disabled, outputs A, B, and C will be the same (inactive outputs yield copies of the previous pair). With a taper assigned to B, Width/Height A and B will both be active with progressively larger intermediate resolutions, and if Taper C is activated, active outputs will be calculated with even finer gradations.

### Final Size & Orientation

Input two integers, get two out in random, landscape, or portrait orientations.

Pretty self explanatory. You can just enter your height/width in the two inputs and then get the requested configurations of WxH or HxW from the two outputs. 

The file random_switch.py two nodes: Final Size & Orientation, and Random Switch (Integer) which was the original, slightly more generalized version. The difference is it is always in "random" mode, so there's no orientation selector.