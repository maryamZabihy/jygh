کنترل همزمان دو LED با استفاده از آردوینو

هدف آزمایش:

هدف از این آزمایش، درک نحوه کنترل چندین خروجی (در اینجا دو LED) به صورت همزمان با استفاده از آردوینو و آشنایی با مفهوم تاخیر در برنامه‌نویسی آردوینو است.

وسایل مورد نیاز:

برد آردوینو

دو عدد LED

مقاومت220

بردبورد

سیم‌های جامپر


توضیحات آزمایش:
در این آزمایش، دو LED به دو پایه خروجی مختلف آردوینو متصل می‌شوند. برنامه‌ نوشته شده  که هر دو LED را به طور همزمان روشن کرده و پس از مدتی خاموش کند این عمل به صورت پی در پی تکرار می‌شود.

کد نرم‌افزاری و توضیحات:


int led1 = 9;  // تعریف پین LED اول
int led2 = 13; // تعریف پین LED دوم


void setup() {
 
  pinMode(led1, OUTPUT);  // تنظیم پین LED اول به عنوان خروجی
 
  pinMode(led2, OUTPUT);  // تنظیم پین LED دوم به عنوان خروجی
}


void loop() {

  digitalWrite(led1, HIGH);  // روشن کردن LED اول
 
  digitalWrite(led2, HIGH);  // روشن کردن LED دوم
 
  delay(5000);               // مکث به مدت 5 ثانیه
  digitalWrite(led1, LOW);   // خاموش کردن LED اول
 
  digitalWrite(led2, LOW);   // خاموش کردن LED دوم
  
delay(500);                // مکث به مدت 0.5 ثانیه
}

تعریف پین‌ها:

در ابتدای برنامه، پین‌های دو LED به متغیرهای led1 و led2 اختصاص داده می‌شوند.

تنظیم حالت پین‌ها:

در تابع setup، هر دو پین به عنوان خروجی تنظیم می‌شوند.

کنترل LEDها:

در تابع loop، ابتدا هر دو LED روشن شده و سپس به مدت 5 ثانیه روشن می‌مانند. پس از آن، هر دو LED خاموش شده و به مدت 0.5 ثانیه خاموش می‌مانند. این چرخه به طور مداوم تکرار می‌شود.
![Screenshot_2024-12-26-01-42-03-074_com miui gallery](https://github.com/user-attachments/assets/2d1d51fe-8c05-4389-8985-edb60712807d)
توضیحات شماتیک:

مقاومت برای محدود کردن جریان عبوری از LEDها استفاده می‌شود و از سوختن آن‌ها جلوگیری می‌کند. مقدار مقاومت بستگی به ولتاژ تغذیه و مشخصات LED دارد.

نتیجه‌گیری:

در این آزمایش، با موفقیت توانستیم دو LED را به صورت همزمان کنترل کنیم و مفهوم تاخیر در برنامه‌نویسی آردوینو را درک کردیم. این آزمایش پایه خوبی برای ساخت پروژه‌های پیچیده‌تر است که در آن‌ها چندین LED یا سایر قطعات الکترونیکی به صورت هماهنگ کنترل می‌شوند.

![IMG_20241226_014536](https://github.com/user-attachments/assets/1cd3dbfe-6ade-4b26-9a4e-8c70c228e3f1)
