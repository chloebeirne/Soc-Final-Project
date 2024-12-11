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
- **VGAColourStripes.v:** This module controls the colours that are being outputted based on the position of the pixels. The original design split the screen into multiple vertical stripes all with a different colour, the original code assigned the colours like this: `if (col >= 0 && col < 210) begin` `red_next <= 4'b0000;` `green_next <= 4'b1111;` `blue_next <= 4'b0000;` `end else if (col >= 220 && col < 430` This logic helped me in understanding of why the pixels were co-ordinated the way they were.

### **Simulation**
I had to make a simulation, and by doing this I understood how the template worked. I used the simulator from Vivado to check the hsync and the vsync and the colour signals over time. The waveform output that was produced by the simulator showed me the timing of the pulses.

### **Synthesis**
After simulation, the next step was synthesis, for this process I had the design template given, and I translated the code into a netlist which could then be used on the FPGA hardware. I used the synthesis tool on Vivado to do this. These reports confirmed that the template design given by our lecturer, had been working with minimal logic and memory which was within the hardware of the development board: Basys 3 Artix 7.

After synthesis, we had implementation where it programmed the design onto the FPGA hardware successfully. The included mapping the bitstream that was generated to the board, from this we can then connect the board to the VGA port on our monitor. When this was completed, we should see the colour stripes start displaying on our screens. Here we can see that the design is functioning correctly, we can also see that the image is displaying smoothly showing the VGA timing signals are synced. The process shows the effectiveness and how modular the design is, it also shows its ready for real world applications.

### **Demonstration**
Once the board was programmed and connected to the VGA port on the monitor, the screen displayed the coloured stripes.
<img src= https://github.com/chloebeirne/Soc-Final-Project/blob/main/docs/assets/images/TempDisplay.png>

## **My VGA Design Edit**
### **Code Adaptation**
The verilog code below is what I adapted to alter the demo template to generate my own personal code, where I just wanted it to generate a simplistic Italian flag. I wanted to show some of my failed tests below:
<img src=https://github.com/chloebeirne/Soc-Final-Project/blob/main/docs/assets/images/green.jpeg>

<img src=https://github.com/chloebeirne/Soc-Final-Project/blob/main/docs/assets/images/code1.jpeg>

This image above isn't at all complex as it seems to display, but it took me a long time to understand how to change from a cycle to cycle and how to make it fit on the display. I was able to create this code with the aid of my lecturer, Michelle Lynch, my class peers, and also online resources from our VLE and ChatGPT.

### **Simulation**
I ran into quite a few issues when it came to my simulation each time I ran my design. A lot of the time, it would say that my simulation would not work due to no error, and then it also told me a few times that some of my code used was not declared, so I had to sift back over my code to see where my errors occurred.

### **Synthesis**
Next for synthesis: this process converted my code into a netlist which made it more usable for the FPGA hardware. I used the tools that are included with Vicado to generate a synthesis report, this told me there were no significant increases in the resource usage against our given template. I believe this is because they both have similar codes and relied on the simple combinational logic for the assigning of the colours and counters for the pixel tracking. 

Included in this, is the useful and helpful insights the synthesis gave me into what optimisations could be added like some logic to reduce delays and also improve the timing performance. 

### **Demonstration**
After finishing all of the previous steps, i can finally generate the design into my board to use the VGA driver to display it onto a monitor. What I saw on my screen was the Italian flag. This showed me that my code worked and there was no bugs to fix.
<img src=https://github.com/chloebeirne/Soc-Final-Project/blob/main/docs/assets/images/italy.jpeg>

### **Hierarchy**
<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
