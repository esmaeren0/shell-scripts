# shell-scripts

Shell script: komutları dosyaya yazıp tekrar çalıştırmayı sağlar. Tekrarlayan işleri otomatikleştirmek için kullanılır.
Syntax:
```
#!/bin/bash  // shebang
```
Örnek:
```
echo "Merhaba Esma"  
```
Çıktı: Merhaba Esma


 # Creating a Shell Script
 
Script dosyası oluştururken ilk satıra shebang (#/bin/bash) yazarız
Syntax:
```
#!/bin/bash
echo "Hello World"
```
#  Executing Shell Scripts

1) bash script.sh ( her türlü çalışır izin olması şart değil)
2)  ./script.sh (çalıştırılabilir izin verilmeli: chmod +x script.sh)
      
Örnek: 
```
./script.sh
```

# Functions

Fonksiyon: Tekrar eden işleri paketleyen kod bloklarıdır.

Syntax:
```
#!/bin/bash

merhabaDunya() {
    echo "Merhaba Dünya"
}

merhabaDunya

```
Çıktı:Merhaba Dünya

#  Variables

Değişken: Bir değeri saklamak için kullanılır.
```
#!/bin/bash
isim="esma" // variable
selamla() {
    echo "Merhaba $1"
}

selamla "$isim"

```

# Exit Command

exit: Scripti hemen durdurur. hata kontrölü için kullanıyoruz.

Syntax: 
```
exit 0 // normal çıkış 
exit 1 //hata ile çıkış
```

Örnek:
```
#!/bin/bash

echo "Başlıyoruz"
if [ "$1" = "" ]; then
    echo "Lütfen bir isim girin!"
    exit 1
fi
echo "Merhaba $1"
echo "Script bitti"
// parametre vermezsek exit 1  verirsek devam eder

```
Çıktı: isim dolu olduğu için devam ediyor


# If / Elif / Else

Koşul kontrolü için kullanılır.
Syntax:
```
if [ koşul ]; then
koşul doğru ise bu blok çalışır
elif [ başka_koşul ]; then
başka koşul doğru ise çalışır
else
hiçbiri doğru değilse
fi
```
Örnek:
```
#!/bin/bash
isim="$1"
if [ "$isim" = "" ]; then
    echo "Lütfen bir isim girin!"
elif [ "$isim" = "Esma" ]; then
    echo "Merhaba Esma"
else
    echo "Merhaba $isim"
fi
```
Parametre boşsa -> “Lütfen bir isim girin!”
Parametre “Esma” ise -> “Merhaba Esma”
Başka bir isim ise -> “Merhaba [isim]”


# User Input

Kullanıcıdan veri almak için read kullanılır.
Syntax:
```
read degiskenAdi
```
Örnek:
```
echo "Lütfen adınızı girin:"
read kullanici
echo  "Merhaba $kullanici"
```




