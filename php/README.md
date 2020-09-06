## [İki sayının toplamını veren algoritma](/php/README.md#soru-1)
Bu algoritmada en fazla 3 değişken kullanabiliriz. Alınan değişkenler toplanarak son değişkene atanır
#### Değişkenler 
```$sayi_1, $sayi_2, $toplam``` olarak belirlendi. Ben 2 değişken kullanarak bitireceğim. Phpyi tarayıcıda değil komut satırında kullanıyorum bu yüzden ```$argv``` globalini kullanıyorum [detaylı bilgi için ziyaret edin](https://www.php.net/manual/en/reserved.variables.argv)
#### Çözüm 
```php 
    $sayi_1 = $argv[1];
    $sayi_2 = $argv[2];
    $sayi_1 += $sayi_2;
    echo $sayi_1;
```
