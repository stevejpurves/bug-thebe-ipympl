# bug-thebe-ipympl

A build of the thebe simple demo that reproduces the the following issues:

1. [resize handle not working](https://github.com/matplotlib/ipympl/issues/501)
   - visit [ipywidgets]()
   - activate and wai on kernel
   - run the first cell
   - try the resize handle
2. multiple ipympl plots interferring with each other
   - visit [ipywidgets]()
   - activate and wait on kernel
   - run the first cell, check the sliders update the plot
   - run the second cell, check the sliders update the plot
   - go back the the first cell and adjust the sliders
   - go back to the second cell and adjust the sliders, the canvas will be rendered as text
   - go back to the first cell, the cell no loger updates
   - re-running any cell will fix that plot
3. placing an ipympl plot in an output does not work as expected, and an inline image is displayed in its place. The same code works as expected in jupyterlab
   - visit [ipywidgets]()
   - activate and wait on kernel
   - run the second cell, check the sliders update the plot
   - hover over the first figure - it is an image output
   - hover over the second figure - it is a jupyter-matplotlib output
   - adjust sliders, these work
   - pick the line on the second figure, this works
