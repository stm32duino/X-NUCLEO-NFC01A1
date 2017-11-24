# X-NUCLEO-NFC01A1

Arduino library to support the X-NUCLEO-NFC01A1 expansion board. The X-NUCLEO-NFC01A1 is a Dynamic NFC tag evaluation board 
to allow expansion of the STM32 Nucleo boards. It is compatible with the Arduino UNO R3 connector layout and it is designed 
around the M24SR64-Y. The M24SR64-Y device is a dynamic NFC/RFID tag IC with a dual interface. It embeds a 64 Kbit EEPROM memory. 
It can be operated from an I2C interface or by a 13.56 MHz RFID reader or a NFC phone.

## Limitation

From I2C interface, you can't write tag with a total size (protocol + payload)
greater than 246 bytes. This is the limitation of the Iblock command on M24SR device.

## Examples

There are several examples with the X-NUCLEO-NFC01A1 library:
* X_NUCLEO_NFC01A1_HelloWorld: This application writes a URI tag on the device. It records an URI.
* X_NUCLEO_NFC01A1_WriteAAR: This application writes a AAR (Android Application Record) tag on the device. It opens an application on your smartphone.
* X_NUCLEO_NFC01A1_WriteMime: This application writes a mime tag on the device. It records a define type of data.
* X_NUCLEO_NFC01A1_WriteSMS: This application writes a SMS tag on the device. It records a SMS body and a recipient phone number.
* X_NUCLEO_NFC01A1_WriteURIMail: This application writes a Mail tag on the device. It records a mail with the recipient, the subject and the body of the message.
* X_NUCLEO_NFC01A1_WriteText: This application writes a Text tag on the device. It records a simple text message.

When the NFC module is started and ready, the message "Sytstem init done!" is displayed on the monitor window.
Next, the tag is written, we wait few seconds, we read the same tag and print it on the monitor window.

You can test this application by connecting it with your smartphone.
On Android, donwload a NFC Tools. Then start the app, check if NFC is activated
on your smartphone. Put your smartphone near the tag, you can read it. You can
write a tag with this app.

## Dependencies

The X-NUCLEO-NFC01A1 library requires the following STM32duino library:

* STM32duino M24SR64-Y: https://github.com/stm32duino/M24SR64-Y

## Documentation

You can find the source files at  
https://github.com/stm32duino/X-NUCLEO-NFC01A1

The M24SR64-Y datasheet is available at  
http://www.st.com/en/nfc/m24sr64-y.html
