# First-program_Vitis

In this tutorial we will see how we can build an application program using vitis sample code from github, we will see eatch and every step to build and run an application program and see the report provides by the vitis toolusing vitis analyzer .

Before we get started lets clone the sample code from github  using the following link below :

git clone https://github.com/Xilinx/Vitis-Tutorials/tree/master/docs/using-multiple-cu

In this tutorial we used the makefile to build and run the application program the makefile is located inside of reference-file

open the terminal and type 

>cd reference-file/

Before we can build the application program we have to set up the environment of vitis and xrt using the following command :

> source /home/namby/Vitis_xilinx/Vitis/2019.2/settings64.sh 

>  source /opt/xilinx/xrt/setup.sh


After that run the command below 

> export XCL_EMULATION_MODE=sw_emu

So now we are ready to build the application program  using the following command :

> make host xclbin TARGET=hw_emu DEVICE=xilinx_u200_xdma_201830_2

after that we can run the application program using the following command :

> make run TARGET=hw_emu DEVICE=xilinx_u200_xdma_201830_2

After running the application program we can see the timeline report generated by the tools using vitis analyzer to do that we can run the command below :

 > vitis_analyzer -open ./timeline_trace.csv






