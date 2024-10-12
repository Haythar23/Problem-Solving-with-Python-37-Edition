import matplotlib.pyplot as plt
from matplotlib.patches import Rectangle, FancyBboxPatch

# Create figure and axes for the flowchart
fig, ax = plt.subplots(figsize=(12, 8))

# Disable axis
ax.set_axis_off()

# Helper function to create shapes with text
def draw_rectangle(ax, center, size, text, color, fontsize=10):
    rect = FancyBboxPatch((center[0] - size[0]/2, center[1] - size[1]/2), size[0], size[1],
                          boxstyle="round,pad=0.3", edgecolor='black', facecolor=color)
    ax.add_patch(rect)
    ax.text(center[0], center[1], text, ha='center', va='center', fontsize=fontsize)

# Drawing shapes and text for the flowchart (similar to the provided example)
# Step 1
draw_rectangle(ax, (-8, 6), (4, 2), 'Identify Leads', 'red')
draw_rectangle(ax, (-2, 6), (4, 2), 'Qualify Leads', 'lightblue')
draw_rectangle(ax, (4, 6), (4, 2), 'Schedule Initial Meeting', 'lightblue')
draw_rectangle(ax, (10, 6), (4, 2), 'Conduct Initial Meeting', 'lightblue')

# Step 2
draw_rectangle(ax, (10, 2), (4, 2), 'Present Product/Service', 'lightblue')
draw_rectangle(ax, (4, 2), (4, 2), 'Address Objections', 'lightblue')

# Step 3 - Contract Preparation and Terms
draw_rectangle(ax, (4, -2), (4, 2), 'Negotiate Terms', 'yellow')
draw_rectangle(ax, (-2, -2), (4, 2), 'Prepare Contract', 'green')

# Step 4 - Close Sale
draw_rectangle(ax, (10, -2), (4, 2), 'Close the Sale', 'yellow')
draw_rectangle(ax, (10, -6), (4, 2), 'Gather Feedback & Testimonials', 'red')

# Drawing arrows
ax.annotate('', xy=(-6, 6), xytext=(-10, 6),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(0, 6), xytext=(-4, 6),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(6, 6), xytext=(2, 6),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(10, 4), xytext=(10, 6),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(10, 2), xytext=(10, 4),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(4, 4), xytext=(4, 6),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(4, 0), xytext=(4, 2),
            arrowprops=dict(facecolor='black', shrink=0.05))
ax.annotate('', xy=(-2, 0), xytext=(-2, 6),
            arrowprops=dict(facecolor='black', shrink=0.05))

# Step for Feedback Loop
ax.annotate('', xy=(10, -4), xytext=(10, -2),
            arrowprops=dict(facecolor='black', shrink=0.05))

# Display the flowchart
plt.tight_layout()
plt.show()
# Problem-Solving-with-Python-37-Edition

Repo for the book: Problem Solving with Python 3.7 Edition by Peter D. Kazarinoff, PhD

A print copy of the book is available on Amazon: [https://www.amazon.com/dp/1693405415](https://www.amazon.com/dp/1693405415)
