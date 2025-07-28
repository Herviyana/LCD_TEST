# LCD_TEST
LCD TEST

#include <Wire.h>
#include <LiquidCrystal_I2C.h>

// Ganti alamat jika perlu, misalnya 0x3F
LiquidCrystal_I2C lcd(0x27, 16, 2); // 16 kolom, 2 baris

void setup() {
  Serial.begin(9600);
  lcd.init();           // Inisialisasi LCD
  lcd.backlight();      // Nyalakan backlight

  Serial.println("LCD 16x2 Test");

  lcd.setCursor(0, 0);
  lcd.print("Hello, Isyarat!");

  lcd.setCursor(0, 1);
  lcd.print("LCD I2C Aktif ✓");
}

void loop() {
  // Tidak ada loop dinamis, hanya untuk tes tampilan
}
