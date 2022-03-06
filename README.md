# CoderCat Asisstant - Kılavuzu

Bu dökümantasyon tüm komutların başına prefix getirildiğini varsayar.
<br>
Prefix: ``/``

## Navigasyon
+ [Aile Komutları](#aile_komutlari)
  + [help](#help)
  + [ping](#ping)
  + [report](#report)
  + [tip](#tip)
+ [Yönetim Ekibi Komutları](#yonetim_ekibi_komutlari)
  + [cli / console](#cli)
    + [get](#cli_get)
    + [set](#cli_set)
    + [add](#cli_add)
    + [remove / rem](#cli_remove)
  + [write](#write)
  + [clear](#clear)
+ [Özellikler](#features)
+ [Güvenlik](#security)

<h2 id="aile_komutlari">Aile Komutları</h2>

<h3 id="help">help</h3>
Yardım içeriğine ulaşın.
<br>
Örnek kullanımlar;

```
help
```

<h3 id="ping">ping</h3>
Yanıt süresini test edin.
<br>
Örnek kullanımlar;

```
ping
```

<h3 id="report">report</h3>
Moderasyon ekibine bir rapor gönderir.
<br>
Örnek kullanımlar;

```
report @x kişisi #genel kanalında insanlara hakaret ediyor!
```

<h3 id="tip">tip</h3>
Öneri kanalında oylanmak üzere bir öneri verirsiniz.
<br>
Örnek kullanımlar;

```
tip Kappa emote getirilebilir.
```

<h2 id="yonetim_ekibi_komutlari">Yönetim Ekibi Komutları</h2>

<h3 id="cli">cli / console</h3>
CoderCat Asisstant kabuğunu kullanarak kök işlemlere erişin, bir terminal kullanmak ile aynı deneyimi sunar. <br>
Referanslar config dosyasından gelmektedir ve yazım biçimi ``.`` ile ayrılan objeler biçimindedir.

<h4 id="cli_get">get</h4>
Belirli parametreleri alın.

<br>
Örnek kullanımlar;

```
cli get cfg
cli get command-log
```

<h4 id="cli_set">set</h4>
Belirli referansları ayarların.

<br>
Örnek kullanımlar;

```
cli set <ref> <deger>
cli set bot.maintenance-mode true
cli set security.root @x
```

<h4 id="cli_add">add</h4>
Belirli referanslara değer ekleyin.
<br>
Örnek kullanımlar;

```
cli add <ref> <deger>
cli add roles.join @x
```

<h4 id="cli_remove">remove / rem</h4>
Belirli referanslardan değer kaldırın.
<br>
Örnek kullanımlar;

```
cli remove <ref> <deger>
cli remove roles.join @x
```

<h3 id="write">write</h3>
Yazılan kanala botun üzerinden bir mesaj gönderin.
<br>
Örnek kullanımlar;

```
write Botlar dünyasından selamlar.
```

<h3 id="clear">clear</h3>
Belirtilen sayıda kanalda mesaj silin.
<br>
Örnek kullanımlar;

```
clear 10
```


<h2 id="features">Özellikler</h2>

+ Bakım modu.
+ Girişte otomatik rol ekleme(üyelik ekranı varsa kuralların kabul edilmesini bekler).
+ İpucu sistemi.
+ Spam/flood koruması.
+ Davet linki koruması.
+ Giriş ve çıkış mesajları.
+ DM giriş mesajı.
+ Tüm işlemlerin kaydını tutar.
+ Davet linki takibi.
+ CoderCat Assistan Shell(terminal üstünden botun kök kontrolünü yapabilme)

<h2 id="security">Güvenlik</h2>

+ Hesap yeni ise private kanala bir uyarı mesajı düşer ve kimin tarafından davet edildiği, hesabın kaç günlük olduğu gibi bilgileri aktarır.
+ Spam ve flood yapılmasını engeller, tekrarı halinde tedbir uygular.
+ CoderCat'in kendi davet bağlantıları da dahil olmak üzere hiçbir şekilde herhangi bir davet bağlantısının üyeler tarafından paylaşılmasına izin vermez.
+ Bir komut çalışmadığında bunu ilgili kişilere bildirmeye çalışır.
