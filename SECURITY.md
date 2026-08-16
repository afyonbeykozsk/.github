# Güvenlik ve Gizlilik Politikası (Security Policy)

Afyon Beykoz Spor Kulübü olarak sporcularımızın, velilerimizin ve kullanıcılarımızın kişisel veri güvenliğine ve sistem bütünlüğüne en üst düzeyde önem veriyoruz.

---

## 🔒 Desteklenen Sürümler

Aşağıdaki tablo, güvenlik güncellemeleri ve yamaları alan aktif sürümleri göstermektedir:

| Bileşen | Sürüm | Güvenlik Desteği |
|---|:---:|:---:|
| **Afyon Beykoz SK Web Platformu** | `v1.x (main)` | :white_check_mark: Destekleniyor |
| **API Backend (NestJS)** | `1.0.0` | :white_check_mark: Destekleniyor |
| **İstemci (Next.js)** | `16.x` | :white_check_mark: Destekleniyor |

---

## 🚨 Güvenlik Açığı Bildirimi (Responsible Disclosure)

Sistemlerimizde potansiyel bir güvenlik açığı veya veri sızıntısı riski tespit ettiyseniz, lütfen bunu **herkese açık issue açarak DEĞİL**, aşağıdaki güvenli kanaldan doğrudan teknik ekibimize iletiniz:

* 📧 **Güvenlik E-Postası:** [guvenlik@afyonbeykozsk.org](mailto:guvenlik@afyonbeykozsk.org)
* ⏱️ **İlk Yanıt Süresi:** 24 saat içinde bildiriminiz incelenir ve teyit edilir.
* 🛡️ **Yama Süreci:** Doğrulanan güvenlik açıkları için en geç 72 saat içinde düzeltme (hotfix) yayınlanır.

Lütfen bildiriminizde aşağıdaki detaylara yer veriniz:
1. Etkilenen bileşen veya API uç noktası (Endpoint).
2. Açığın tetiklenmesi için gerekli adımlar (Proof of Concept - PoC).
3. Potansiyel etki analizi (Veri erişimi, yetki yükseltme vb.).

---

## 📜 KVKK ve Veri Koruma Taahhüdü

Kulübümüz sistemlerinde 6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK) gereğince:
* Kimlik ve iletişim verileri şifrelenmiş ve kör-indeksli (blind-indexed) olarak saklanır.
* Özel nitelikli sağlık verileri yalnız yetkili personel tarafından açık rıza şartıyla işlenir.
* Tüm veri tabanı ve API erişimleri değiştirilemez denetim logları (Audit Logs) ile kayıt altına alınır.

İlginiz ve desteğiniz için teşekkür ederiz.
