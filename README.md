# Rappels de microcontrôleurs
## Erreurs recontrés en Ubuntu 24 et solutions
### libncurses5 missing
> Could not determine GDB version using command: /opt/st/stm32cubeide_1.2.0/plugins/com.st.stm32cube.ide.mcu.externaltools.gnu-tools-for-stm32.7-2018-q2-update.linux64_1.0.0.201904181610/tools/bin/arm-none-eabi-gdb --version

Source: [Reddit post: libncurses5-dev?](https://www.reddit.com/r/Ubuntu/comments/1cm97bg/libncurses5dev/). Issue: libncurses5 was removed in 24.04.   

**Solution:**  
```bash
wget http://archive.ubuntu.com/ubuntu/pool/universe/n/ncurses/libtinfo5_6.4-2_amd64.deb && sudo dpkg -i libtinfo5_6.4-2_amd64.deb && rm -f libtinfo5_6.4-2_amd64.deb

wget http://archive.ubuntu.com/ubuntu/pool/universe/n/ncurses/libncurses5_6.4-2_amd64.deb && sudo dpkg -i libncurses5_6.4-2_amd64.deb && rm -f libncurses5_6.4-2_amd64.deb

sudo apt install lib32ncurses5-dev libncurses5 libncurses5-dev -y```

