# NodeMCU (Arduino) - RTC init from NTP

This is an example sketch (quick and dirty) to show how I initialized a [DS1307 RTC Module](https://learn.adafruit.com/ds1307-real-time-clock-breakout-board-kit/understanding-the-code) from a NTP server's response.   
The PIO configuration is for a NodeMCU v1.0 board, which can be modified as required.
## Changing Timezone
Change the following constant to your timezone offset from GMT in seconds:
```cpp
const uint32_t timeZoneOffsetSeconds = 19800;
```

## References

 1. [TimeNTP_ESP8266WiFi.ino example from the "Time" library](https://github.com/PaulStoffregen/Time/tree/master/examples/TimeNTP_ESP8266WiFi)
 2. [Arduino Forum Post on improving NTP received time's accuracy](https://forum.arduino.cc/t/heres-how-to-get-a-more-accurate-rtc-clock-set-from-an-ntp-time-server/506179/3)
 3. [PlatformIO - Fix SPI.h "no such file" error](https://techoverflow.net/2020/12/14/how-to-fix-platformio-esp8266-esp32-fatal-error-spi-h-no-such-file-or-directory/)
 4. [RTClib.h - `toString()` Documentation](https://adafruit.github.io/RTClib/html/class_date_time.html#a27aad4b627b20de84c23d2b0ed657cba)