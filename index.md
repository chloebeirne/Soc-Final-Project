---
FPGA VGA Driver Project
---

My name is Chloe Beirne, and this is my VGA Driver Project. For my project, I wanted to make the Swedish flag, but it didn't work after a lot of work and research, so I decided to create an easier image, of the Italian flag.

## **Template VGA Design**
### **Project Set-Up**
The template design was an easy to follow demo on how to add the VGA signal generation. It showed vertical stripes of a series of seven colours.

I set up my project in Vivado, and I made sure that all of my design files were added and ready to simulate, synthesis and implement. I used all of the parameters provided from Vivado to check the design flow, resource usage and timing for the project. Below, i will show an image of my project summary showing the setup and design flow.

<img src= "https://github.com/chloebeirne/Soc-Final-Project/blob/main/docs/assets/images/photo7.png">

### **Template Code**
The key modules in this project were:
- **VGASync.v:** This module makes the horizontal and vertical sync signals, this tracks      the current position of each pixel that's being displayed on screen, we can then ensure     that the display is being updated row by row, and frame by frame by using both a            horizontal and ertical count.
- **VGAColourStripes.v:** 
### **Simulation**
Explain the simulation process. Reference any important details, include a well-selected screenshot of the simulation. Guideline: 1/2 short paragraphs.
### **Synthesis**
Describe the synthesis and implementation processes. Consider including 1/2 useful screenshot(s). Guideline: 1/2 short paragraphs.
### **Demonstration**
Perhaps add a picture of your demo. Guideline: 1/2 sentences.

## **My VGA Design Edit**
Introduce your own design idea. Consider how complex/achievabble this might be or otherwise. Reference any research you do online (use hyperlinks).
### **Code Adaptation**
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.
### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
