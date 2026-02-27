# XC2064-in-2026
a easy way to initialize XC2064-PD48 in 2026
# XC2064 in 2026 🚀

A minimalist, AI-collaborative project to awaken the 1986 Xilinx XC2064-PD48 using an STM32F103.

## 📖 Something I want to say
I use an **STM32F103C8T6** to load the bitstream. 
The bitstream is generated using a patched **XACTSTEP 5.0.0** (found at bitsavers.org). 

**Collaboration:** This project is a result of human-AI teamwork. I designed the architecture and logic flow, while **Gemini** generated the C code based on my descriptions.

## 🛠️ How to Use
1. **Generate:** Install XACTSTEP in a virtual machine (Windows 95/98 recommended). Use it to design your logic and export the `.RBT` file.
2. **Transfer:** Move the `.RBT` file to your modern PC. Drag and drop it onto `XC_Workstation.exe`. The software will process the bitstream and prepare for serial transmission.
3. **Connect:** Use a CH340 (USB-to-TTL) to connect your PC to the STM32's **USART2** (Baud rate: **4800**).
4. **Flash:**
   - Set the COM number in `XC_Workstation.exe`.
   - Press **"传输字节流"** (Transfer Bitstream) to push data to the MCU.
   - Press **"开始装载"** (Start Loading) to flush the bitstream into the XC2064.
5. **Verify:** Use a voltmeter to measure the **D/P** pin. If it goes **High**, you have succeeded!

## 🔌 Hardware Notes
- **Wiring:** Please check the uploaded image for the full breadboard diagram.
- **OLED (Optional):** You can connect a small OLED (SCK -> PB8, SDA -> PB9) to see real-time loading details. If you don't have one, just ignore it.

## ⚠️ Disclaimer
Logic by me, code by AI. No support, no comments, no warranties. If you have better ideas, fork it and make it yours.

**Stay curious. Stay punk.**
