<p align="center">
  <a href="https://github.com/williamFalcon/deep-learning-gpu-box-build-instructions">
    <img alt="GPU box" src="https://github.com/williamFalcon/deep-learning-gpu-box-build-instructions/blob/master/gpu_box.jpeg" width="400">
  </a>
</p>
<h3 align="center">
  Deep Learning GPU box build instructions   
</h3>
<p align="center">
  Instructions to build your own research GPU box for deep learning AND get it set up with tensorflow, pytorch and CUDA drivers.   
</p>




#### After following these instructions you'll have:   
1. A sick GPU box with multuple GPUs set up.   
2. A functional OS ready for deep learning.   


## Parts   

| Part | Brand / Link | Purpose | Quantity | Optional? |
|---|---|---|---|---|
| M2 Harddrive | [Samsung 970 EVO 2TB - NVMe PCIe M.2 2280 SSD (MZ-V7E2T0BW) ](https://www.amazon.com/dp/B07C8Y31G1/?tag=pcpapi-20)   | OS + working dir   | 1   | N|
| SSD | [Samsung 860 EVO 4TB 2.5 Inch SATA III Internal SSD (MZ-76E4T0B/AM)](https://www.amazon.com/dp/B07864XY8B/?tag=pcpapi-20)   | fast data loading. Keep datasets not in use on the SSHD   | 2  | N |
| Processor | [Intel i7 (6+ cores)](https://www.amazon.com/Intel-i7-6900K-Processor-2011-v3-BX80671I76900K/dp/B01FJLAIG0/ref=sr_1_3?s=electronics&ie=UTF8&qid=1537003449&sr=1-3&keywords=Intel+-+Core+i7-6900K)   | At least 1 core per GPU | 1 | N |
| Power source | [Corsair 1500 W](https://www.amazon.com/gp/product/B00MFJ4OBA/ref=oh_aui_detailpage_o07_s03?ie=UTF8&psc=1)   | Enough for 4 gpus | 1 | N |
| Motherboard | [ASUS LGA2011-v3 Dual 10G LAN 4-Way GPU ATX/CEB Motherboard (X99-E-10G WS)](https://www.amazon.com/dp/B01LEXRW48/?tag=pcpapi-20)   | Big enough for 4 GPUs | 1 | N |  
| RAM | [Corsair Vengeance RGB 64GB (4x16GB) DDR4 3333MHz C16 Desktop Memory - Black)](https://www.amazon.com/dp/B072JYJFB9/?tag=pcpapi-20&th=1)   | You need at least as much RAM as GPU RAM | 2 | N |  
| Tower | [Phanteks Enthoo Pro](https://www.amazon.com/dp/B00K6S1B3Q/ref=dp_prsubs_2) | Big enough for 4 GPUs | 1 | N |   
| GPUs | [NVIDIA 1080Ti](https://www.amazon.com/gp/product/B06Y13N2B6/ref=oh_aui_detailpage_o01_s00?ie=UTF8&psc=1) | Go with 12 GB RAM. Best price/teraflops+RAM out there. (Optional jet fans vs open fan. I use both) | 4 | N |   
| CPU Water Cooler | [Corsair CW-9060027-WW Hydro Series H115i](https://www.amazon.com/gp/product/B019955RNQ/ref=oh_aui_detailpage_o07_s02?ie=UTF8&psc=1) | Try to keep the overall temp in the box down or GPUs will throttle. (Optional but HIGHLY recommended) | 1 | Y |   
| Small Fans | [Corsair ML120 Pro LED](https://www.amazon.com/gp/product/B01G5I6MUW/ref=oh_aui_detailpage_o06_s00?ie=UTF8&psc=1) | Replace front and bottom pannel fans. These are more quiet than the stock fans | 3 | Y |   
| Large Fans | [Corsair ML140 Pro LED](https://www.amazon.com/gp/product/B01G5I6Q94/ref=oh_aui_detailpage_o01_s00?ie=UTF8&psc=1) | Assuming you get rid of the tower stock fans. (Highly recommended) | 4 | Y |   
| FAN connectors | [4Pin PWM to 3Pin](https://www.amazon.com/gp/product/B01H0OZC9W/ref=oh_aui_detailpage_o01_s00?ie=UTF8&psc=1) | You'll run out of fan connectors with new fans | 1 | Y |   


### Considerations   
1. Temperature
    - If your machine gets too hot, the GPUs will auto-throttle down.   

2. Bottlenecks
    - With deep learnning, the biggest bottleneck is not the GPU but the DATA TRANSFER to the GPUs.
    - This is why the Motherboard needs to be fast enough and should have at least 40 PCI lanes.  
    - The drives need to be really fast.   
    - Use the SSD to feed data directly to model. Use SSHD for long term storage that won't go into the model directly.   

3. RAM
    - Have at least as much RAM as you have GPU RAM.   

4. CPU   
    - Have at least 1 core per GPU. 
    - Water cooling can help keep the overall temperature low.   
    
### Assembly / Install instructions    

I'll add more details later, but in order you should:   
1. Install fans.   
2. install motherboard.   
3. Install power source (but don't screw in yet).   
4. Connect all the fans to motherboard.   
5. Install drives.   
6. Connect drives to motherboard.   
7. Connect motherboard to power supply. 
8. Connect power button, usb, etc... to motherboard.
9. Install GPUs.  
10. Connect GPUs to power supply. 
11. Install RAM.   
12. Screw in powersource.   
13. Fix all the cables neatly.   
14. Insert an ubuntu live USB.   
15. Turn on.   
16. Pray.    
16. Boot into BIOS and set the USB as the priority drive.   
17. Install Ubuntu (or your OS).   
18. Follow [these instructions](https://github.com/williamFalcon/tensorflow-gpu-install-ubuntu-16.04) to set up your system with tensorflow, pytorch and cuda drivers.      
19. Learn deeply.   


### Some deep learning tips    
1. Log your experiments and parallelize hyperparameter search using [the python library test tube](https://github.com/williamFalcon/test-tube).   

