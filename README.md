# 高速ADC
采用STM32F407的DCMI接口以及AD9283制作采样率高达100M的ADC

采用FPGA的adc对信号进行采集以后，对数据处理麻烦，并且FPGA造价相对较贵，所以采用32自制一块高速ADC
采样率理论值是100MSPS，但是受限于DCMI接口的速率，实际只能到65MSPS左右

代码只提供DMCI和AD9283的代码驱动，具体采样数据如何处理（DMA接收数据为32位，采样数据为8位），请自行更改。
此文章介绍的是8位的AD9283，不采用FIFO，后续将会更改为12位的AD9235使ADC精度更高，以及内部提供时钟，不需要外部时钟。
