# PYNQ RFSoC Workshop

A collection of designs and notebooks for the PYNQ &amp; RFSoC workshop — part of the ZCU111's [v2.4.1 PYNQ image](http://www.pynq.io/board.html).

<img src="https://github.com/xilinx/pynq_rfsoc_workshop/blob/master/notebooks/assets/preview/preview_qpsk.png" align="left"  width="30%"/>
<img src="https://github.com/xilinx/pynq_rfsoc_workshop/blob/master/notebooks/assets/preview/preview_sdfec.png" align="left" width="30%"/>
<img src="https://github.com/xilinx/pynq_rfsoc_workshop/blob/master/notebooks/assets/preview/preview_dsp.png" width="30%"/>

## Getting started

These notebooks are already included in the ZCU111's v2.4.1 PYNQ image. The steps to get started with this image are:

  1. Download the "ZCU111 v2.4.1 PYNQ image" file from the [PYNQ website](http://www.pynq.io/board.html).
  
  2. Refer to the PYNQ docs for steps to:
     * [burn the image](https://pynq.readthedocs.io/en/latest/appendix.html#writing-the-sd-card) to an SD card, and
     * [configure your network interface](https://pynq.readthedocs.io/en/latest/appendix.html#assign-your-computer-a-static-ip-address)
    
  3. Navigate to `http://<IP address>/lab` for the new JupterLab interface. We use features that aren't in the default interface.
     
  4. Attach a SMA loopback cable between the DAC/ADC pair as shown below.

<p align="center">
<img src="https://github.com/strath-sdr/rfsoc_qpsk/blob/master/img/rfsoc_setup.png" width="800">
</p>

Now you're ready to use the notebooks in the `rfsoc_workshop` folder, as highlighted below:

<p align="center">
<img src="https://github.com/xilinx/pynq_rfsoc_workshop/blob/master/notebooks/assets/preview/launcher_highlight.png" width="800">
</p>

## Building from source

> This step is *optional*. Only continue if you want to build your own image.

You can recreate this workshop manually if, for example, you want to use it on a different PYNQ image.
Clone this repo and manually install the constituent RFSoC overlays:
  1. [RFSOC-QPSK](https://github.com/strath-sdr/rfsoc_qpsk)
  2. [SDFEC-PYNQ](https://github.com/Xilinx/SDFEC-PYNQ)
  3. [DSP-PYNQ](https://github.com/Xilinx/DSP-PYNQ)

Run `make install` to deploy the workshop notebooks to the `rfsoc_workshop` folder.

## Hosting a lab session

Note that there is a `make install` target that will replace the notebooks with the original copies. Use this to do a soft reset between groups.

## License 

[BSD 3-Clause](https://github.com/Xilinx/PYNQ_RFSOC_Workshop/blob/master/LICENSE)
