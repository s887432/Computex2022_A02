# Computex2022_A02
egt dashboard code

download linux4sam-2021.04 <br>
$ git clone https://github.com/linux4sam/buildroot-at91.git -b linux4sam-2021.04<br>
$ git clone https://github.com/linux4sam/buildroot-external-microchip.git -b linux4sam-2021.04<br>

put patch to folder<br>
$ cd buildroot-external-microchip<br>
$ git apply ../0000-buildroot-external-microchip-fastboot-net-based-linux4sam-2021.04.patch<br>

$ cd ../buildroot-at91<br>
$ BR2_EXTERNAL=../buildroot-external-microchip make sam9x60ek_graphics_dashboard_sd_defconfig<br>
$ make menuconfig<br>

add paho-mqtt-c, paho-mqtt-cpp, mosquitto<br>

$ make -j32<br>

put motorcycledash.cpp to output/build/egt-egt-dashdemo/examples/motorcycledash/<br>
put Makefile to output/build/egt-egt-dashdemo/examples<br>

$ make -C output/build/egt-egt-dashdemo/examples<br>

by Patrick Lin
@ Taipei, 2022/04/29
