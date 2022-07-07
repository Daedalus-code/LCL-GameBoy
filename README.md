# LCL GameBoy 3B+ RetroPi Clean Install (full control)  

Copy the file ```mzdpi6.dtbo``` from LCL ```overlay``` directory to the new ```overlay``` directory.

edit /boot/config.txt to look like this.

```audio_pwm_mode=1

disable_audio_dither=1
display_default_lcd=1
display_rotate=3

dpi_group=2
dpi_mode=87
dpi_output_format=0x07f006

dtoverlay=mzdpi6,pwm-2chan,pin=18,func=2,pin2=13,func2=4
dtparam=i2c_arm=off,i2s=off,spi=off,audio=on

enable_dpi_lcd=1
enable_uart=0

framebuffer_height=320
framebuffer_width=460

gpio=18=op,dh,pd
gpu_mem=128

hdmi_timings=320 0 28 18 28 480 0 2 2 8 0 0 0 60 0 32000000 1
max_usb_current=1
overclocking.md
start_x=0

# END
