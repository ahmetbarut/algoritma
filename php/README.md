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
## [Girilen 2 sayının karesini hesaplayan algoritma](/php/README.md#soru-2)
Bu soruda kullanıcının girdiği 2 sayının karesini hesaplayacak php'de üsleri çarpmak için ```**``` operatörü kullanılır. Örnek kullanımı çözümde mevcut. 
#### Çözüm 
```php
    $sayi_1 = $argv[1];
    $sayi_2 = $argv[2];
    $sayi_1 **= $sayi_2;
    echo $sayi_1;
```
## [Yaş Hesaplama](/php/README.md#soru-3)
Kullanıcı doğum tarihini girerek yaşını hesaplayan algoritma. Ben [date](https://www.php.net/manual/tr/function.date) fonksiyonunu kullanarak bu günün yılını aldım detay için bakınız.
#### Çözüm 
```php
    $doğum_yılı = (int) $argv[1];
    $yaş = date("Y") - $doğum_yılı;
    echo "Yaşınız  => {$yaş} \n" ;
```
## [Pozitif sayılarda toplama işlemi kullanarak çarpma işlemi yapan algoritma](/php/README.md#soru-4)
Pozitif sayıları toplayarak çarpma işlemi yapma burda döngü kullanmam gerekiyor. 3 adet değişken ```$sayi_1, $sayi_2, $toplam```.
```php
    $sayi_1 = $argv[1];
    $sayi_2 = $argv[2];

    $toplam = 0;

    for ($i = 0; $i < $sayi_1; $i++) {
        $toplam += $sayi_2;
    }
    echo $toplam . "\n";
```
Kodları açıklayayım. For döngüsünde `$i = 0` dedim 0'dan başlayacak `$i < $sayi_1` 0'dan başlayıp belirttiğim değişkendeki sayı boyunca dönecek ben 6 verdim yani döngü 0'dan 5'e kadar gelecek bu da 6 kez dönüyor. `$i++` her seferinde 1 defa arttırır.
Her döndüğünde `$toplam` değişkenine `$sayi_2`'yi ekler zaten amacımız 2. sayıyı 1. sayı kadar toplamak veya tam terside olabilir.
## [Kelime Arama](/php/README.md#kelime-arama)
Bir paragraf içinde arama yapmak. Ben bu şekilde yaparak hallettim. 2 parametre alır. 
1. parametre `$kelime`, 2. parametre `$dizge` `explode` yöntemiyle dizgeyi parçalamamız gerekiyor kelimeleri karşılaştırmak için. 
`for` döngüsünü 0'dan başlatıp `$dizge` uzunluğuna göre sınırladık `explode` yöntemi dizgeyi dizi haline getiriyor. 
```php 
        $kelime = "#title1";
        $dizge = explode(" ", "#title1 Merhaba Dünya !");
        for ($i = 0; $i < count($dizge); $i++) {
            if ($dizge[$i] == $kelime) {
                echo "Eşit";
            }
        }

```