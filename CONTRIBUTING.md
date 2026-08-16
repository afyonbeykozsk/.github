# Katkı ve Geliştirme Standartları (Contributing Guide)

Afyon Beykoz Spor Kulübü yazılım projelerine katkıda bulunurken aşağıdaki kurumsal mühendislik ve güvenlik kurallarına uyulması zorunludur.

---

## 🌿 1. Git ve Dal (Branch) Stratejisi

- `main` dalı her zaman üretime hazır, stabil ve tek kanonik kaynaktır.
- `main` dalına doğrudan commit veya push yapılmaz.
- Tüm geliştirmeler kısa ömürlü görev dallarında (`feature/...`, `fix/...`, `chore/...`) yapılır.
- Çalışmalar tamamlandığında Pull Request (PR) açılarak CI testlerinin ve bağımsız kod incelemesinin geçmesi beklenir.

---

## 🧪 2. Kalite ve Test Kapıları

Bir Pull Request açılmadan önce yerelde aşağıdaki kontrollerin tamamının yeşil (PASS) olması şarttır:

```bash
pnpm --filter server run lint:check
pnpm --filter server run typecheck
pnpm --filter server run test

pnpm --filter client run lint
pnpm --filter client run typecheck
pnpm --filter client run test
```

---

## 🛡️ 3. Güvenlik ve KVKK Hijyeni

- **Sıfır Gerçek Veri:** Kod tabanına, test fixture'larına veya commit mesajlarına asla gerçek TCKN, telefon, e-posta, sağlık verisi veya production secret'ı konulmaz.
- **Şifreli Depolama:** Hassas kimlik verileri blind-index ve şifreleme sözleşmelerine uygun işlenir.
- **Disposable Testler:** Veritabanı testleri yalnız disposable/Testcontainers ortamında doğrulanır.

---

## 📝 4. Commit ve Mesaj Standartları

Commit mesajlarında [Conventional Commits](https://www.conventionalcommits.org/) standardı kullanılır:
- `feat:` Yeni bir özellik eklendiğinde.
- `fix:` Bir hata düzeltildiğinde.
- `refactor:` Davranışı değiştirmeyen mimari düzenlemelerde.
- `test:` Testler eklendiğinde veya güncellendiğinde.
- `docs:` Dokümantasyon güncellemelerinde.
