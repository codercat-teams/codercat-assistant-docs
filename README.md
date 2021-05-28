# CoderCat Asisstant - Klavuzu

Bu dökümantasyon tüm komutların başına prefix getirildiğini varsayar.
<br>
Prefix: ``/``

## Navigasyon
+ [Aile Komutları](#aile_komutlari)
  + [help](#help)
  + [ping](#ping)
  + [report](#report)
  + [tip](#tip)
+ [Moderasyon Komutları](#moderasyon_komutlari)
  + [cli / console](#cli)
    + [get](#cli_get)
    + [set](#cli_set)
    + [add](#cli_add)
    + [remove / rem](#cli_remove)
  + [write](#write)
  + [clear](#clear)
  + [ban](#ban)
  + [mute](#mute)
  + [unban](#unban)
  + [unmute](#unmute)
  + [kick](#kick)
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

<h2 id="moderasyon_komutlari">Moderasyon Komutları</h2>

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

<h3 id="ban">ban</h3>
Etiketlenen kullanıcıların süre belirtmeden ya da belirli bir süre için yasaklayın. Süre dakika cinsindendir ve en az 1 dakika verilebilir.
<br>
Örnek kullanımlar;

```
ban @x @y @z    -> x, y ve z üyelerini süre olamadan yasakla.
ban 1 @x @y @z  -> z, y ve z üyelerini 1 dakika süre ile yasakla.
```

<h3 id="mute">mute</h3>
Etiketlenen kullanıcıların süre belirtmeden ya da belirli bir süre için susuturun. Süre dakika cinsindendir ve en az 1 dakika verilebilir.
<br>
Örnek kullanımlar;

```
mute @x @y @z    -> x, y ve z üyelerini süre olamadan sustur.
mute 1 @x @y @z  -> z, y ve z üyelerini 1 dakika süre ile sustur.
```

<h3 id="unban">unban</h3>
Etiketlenen kullanıcıların yasaklamasını kaldırın.
<br>
Örnek kullanımlar;

```
unmute @x @y @z
```

<h3 id="unmute">unmute</h3>
Etiketlenen kullanıcıların susuturlmasını kaldırın.
<br>
Örnek kullanımlar;

```
unmute @x @y @z
```

<h3 id="kick">kick</h3>
Etiketlenen kullanıcıları atın.
<br>
Örnek kullanımlar;

```
kick @x @y @z
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
