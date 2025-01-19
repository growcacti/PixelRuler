# PixelRuler
Onscreen Pixel Ruleri


This code defines a draggable ruler utility using the tkinter library in Python. The main features are:
Overview of Key Components:
Class DraggableRuler

    A subclass of tk.Toplevel, representing a draggable window containing a ruler.
    Parameters:
        root: The parent window (usually the main Tkinter application root).
        orientation: Specifies the ruler's orientation ('horizontal' or 'vertical').
    Main Attributes:
        self.orientation: Stores the ruler's orientation.
        self.is_dragging: Tracks whether the ruler is being dragged.
        self.canvas: A canvas widget where the ruler's markings are drawn.

Methods:

    __init__
        Initializes the draggable ruler.
        Makes the window borderless (overrideredirect(True)) and keeps it on top (attributes('-topmost', True)).
        Creates a Canvas to draw the ruler's markings and binds mouse events for dragging.
    draw_ruler
        Draws the ruler's markings based on the orientation:
            Horizontal ruler:
                Width: 1800 pixels, Height: 40 pixels.
                Major tick marks and labels every 100 pixels and minor tick marks every 10 pixels.
            Vertical ruler:
                Width: 40 pixels, Height: 1000 pixels.
                Major and minor tick marks are drawn similarly to the horizontal ruler.
    start_drag
        Triggered by the <Button-1> event (mouse left button press).
        Captures the starting position of the drag.
    do_drag
        Triggered by the <B1-Motion> event (mouse movement with the left button pressed).
        Updates the position of the ruler window as the mouse moves.
    stop_drag
        Triggered by the <ButtonRelease-1> event (mouse left button release).
        Stops the drag operation.

Main Program Execution

    The main block:
        Creates a hidden root window using root.withdraw().
        Instantiates two draggable rulers: one horizontal and one vertical.
        Starts the Tkinter event loop with root.mainloop().

Features and Behavior

    Borderless, Always-on-Top Window:
        The rulers appear without standard window decorations (no title bar or borders).
        They remain on top of other windows.

    Draggable Window:
        Users can click and drag the rulers to reposition them.

    Customizable Orientation:
        The orientation parameter determines whether the ruler is horizontal or vertical.

    Dynamic Tick Marking:
        Major and minor ticks are drawn at regular intervals (e.g., every 10 pixels, with labels every 100 pixels).

Potential Use Cases

    Useful for UI designers, developers, or anyone needing a virtual measuring tool.
    Can serve as a visual aid for aligning or measuring elements on a screen.


Possible Enhancement

    Resizable Ruler:
        Add functionality to resize the ruler dynamically.
    Customizable Dimensions:
        Allow users to specify the length and width of the ruler at runtime.
    Improved Appearance:
        Add colors, gradients, or transparency for a modern look.
    Scaling Support:
        Add zooming or scaling functionality to adjust the tick spacing.


    
