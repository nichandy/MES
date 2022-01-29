# Exercise 8: Memory Maps and Linker Files
Compile your project code so it prints out the heap pointer and the stack pointer. Print out a global variable address. If you can find it, modify your linker file to swap your uninitialized variables and initialized variables. Verify it is as expected in the memory map. See how that changes your code output. 

## STM32F0 Discovery Specs

| MCU           | Series                | Flash       | RAM         |
| -----------   | -----------           | ----------- | ----------- |
| STM32F051R8T6 |  ARM Cortex M0+       | 64 Kb       | 8 Kb        |

```
Memory Configuration

Name             Origin             Length             Attributes
RAM              0x20000000         0x00002000         xrw
FLASH            0x08000000         0x00010000         xr
*default*        0x00000000         0xffffffff
```
