# AmrasElessar (Profile) · Repo Standards

> **Hedef konum:** `C:\Projeler\AmrasElessar\REPO_STANDARDS.md`
> Reponun köğüne kopyalayıp commit'leyin. Sonraki düzenlemeler bu dosyaya bağlı kalmalı — değişiklik gerekirse burayı da güncelleyin.
>
> **Snapshot:** 2026-05-14 (D Brand README + about/topics align sonrası — profil reposu)
> **ℹ️ Bu repo GitHub'ın özel "profile README" reposudur** — `github.com/AmrasElessar`'da görünen README'yi barındırır. Diğer D Brand repolarından farklı role sahip.

---

## 1. Locked GitHub metadata

| Alan | Değer |
|---|---|
| **Owner/Repo** | `AmrasElessar/AmrasElessar` |
| **Visibility** | public (profile repo zaten public olmalı) |
| **Default branch** | `main` |
| **License (SPDX)** | (boş — profile repo için lisans gerekmez; sadece README içeriği var) |
| **Description** | `D Brand · Solo indie developer building AI-native, local-first, open-source tools for Windows & Android — TR/EN.` |
| **Homepage** | (boş) |
| **Topics** | (yok — profile repolarında topic eklenmez, görünmez) |

Değişiklik yaparsanız bu tabloyu güncelleyin + `gh repo edit` ile remote'a yansıtın.

---

## 2. README iskeleti (Profile özel yapı — D Brand uyumlu)

Bu repo standart D Brand README iskeletini **kullanmaz** — profil reposunun farklı bir görev tanımı vardır: kişiyi tanıt + D Brand ürünlerini sergile + iletişim kanallarını göster.

### 2.1 Bölüm sırası (kanonik — profile için)

1. **Header** — center-aligned: ad + rol + alt etiket + badge satırı (Email, GitHub, Sponsor, Latest release link) + profile view counter
2. **🇹🇷 Hakkımda** + **🇬🇧 About** — bilingual self-intro
3. **🎯 D Brand Felsefesi · Philosophy** — Privacy First · Local by Default · vb. tablo
4. **📦 D Brand Ailesi / Family** — 8 D Brand repo kartları (her biri kısa açıklama + repo link)
5. **🛠️ Teknoloji / Tech Stack** — kullanılan tüm dil/framework badge'leri (D Brand genelinde)
6. **📈 İstatistikler / Stats** — GitHub stats widget (shields.io tabanlı, Vercel widget'ları yerine — daha önce kırılmıştı bunlar `a31a75d` commit'inde değiştirildi)
7. **💖 GitHub Sponsors** — bağış kanalları
8. **📬 İletişim / Contact** — email + sosyal kanallar

### 2.2 Header pattern

```markdown
<div align="center">

# Orhan Engin OKAY

### `D Brand` · Indie Developer · Türkiye 🇹🇷

**AI-native · Local-first · Open-source where possible**

[![Email](...)](mailto:...)
[![GitHub](...)](https://github.com/AmrasElessar)
[![Sponsor](...)](https://github.com/sponsors/AmrasElessar)
[![D-Terminal](...)](https://github.com/AmrasElessar/d-terminal/releases/latest)

[![Profile views](https://komarev.com/ghpvc/?username=AmrasElessar&...)](https://github.com/AmrasElessar)

</div>
```

### 2.3 D Brand Family kart yapısı

Her kart için tutarlı format (örnek):

```markdown
### 🖥️ D-Terminal
**Agent-aware Windows terminal — Tauri v2 + Vue 3 + Rust**
*Tek pencerede çoklu shell, AI entegrasyonu, uzmanlaşmış pane tipleri*

[→ Repo](https://github.com/AmrasElessar/d-terminal) · [→ Releases](https://github.com/AmrasElessar/d-terminal/releases) · GPL-3.0+ · pre-alpha
```

8 kart (alfabetik veya status önceliğine göre):
1. D-Terminal — pre-alpha, GPL-3.0+, Windows
2. D-Space — alpha/MVP, GPL-3.0+, Windows
3. D-Watchtower — alpha, GPL-3.0+, Android (private→public)
4. D-Transfer — pre-alpha, GPL-3.0+, Windows + Linux
5. D-Car Launcher — alpha, GPL-3.0+, Android (private→public)
6. AdminPDFToolkit — stable, AGPL-3.0+, Web/PWA/Windows service
7. D-Player — MVP, Proprietary (Premium), Android
8. Kael'in Kaderi — alpha · WIP, TBD lisans, Android (private)

### 2.4 Bilingual yapı

- TR ve EN section'ları yan yana (`<table>` veya alt alta), profil reposu özel olduğundan `<details>` yerine açık tutulur.

---

## 3. Tech stack notu (sergilenen)

Profile reposunda D Brand genelindeki tüm tech stack sergilenir:
- **Languages:** Rust, Kotlin, TypeScript, Python, C++17
- **Frameworks:** Tauri v2, Vue 3, Jetpack Compose, Capacitor, Flask/FastAPI
- **Targets:** Windows, Android, Linux, Web/PWA

---

## 4. Lisans (profile reposu)

- Profile repolarında LICENSE dosyası **gerekmez** — sadece README içeriği vardır.
- README içeriği için isteğe bağlı CC BY 4.0 veya benzer atıf-uyumlu lisans eklenebilir (zorunlu değil).

---

## 5. Commit mesaj stili

Conventional commits — recent log'dan gözlemlenen örnekler:

- `feat(readme): ...` — yeni bölüm/kart/badge
- `fix(readme): ...` — kırık link/widget/typo (örn. `a31a75d`: vercel widget'lar kırıktı, shields.io'ya geçildi)
- `chore: ...` — FUNDING.yml gibi config (örn. `b05e6a0`, `0553ae4`)

Dil: TR veya EN; recent log TR ağırlıklı.

---

## 6. Dosya hijyeni

- Adı `:` veya `\` içeren dosyalar **commit'lenmez** — `C:Temp...` formundaki kalıntılar (yol parse hatası) silinir: `git clean -f`. Bu repoya başka repoların README draftları sızabiliyor — push öncesi mutlaka `git status` kontrol.
- **Zorunlu:** `README.md`, `.github/FUNDING.yml` (Sponsors için)
- **Tercih edilen:** boş ya da minimal — profil reposu hafif tutulur.

---

## 7. Repo-spesifik notlar

- **Profile repo özel görev** — github.com/AmrasElessar'da görünen public profil sayfası. README'deki sıralama, kart yapısı, badge'ler doğrudan kullanıcının marka algısını şekillendirir.
- **Komarev profile view counter** — kalıyor; alternatif yok şu an.
- **Shields.io tercih edilir, Vercel widget'lardan kaçınılır** — `a31a75d` commit'inde Vercel kırılmıştı, shields.io'ya geçildi. Bu karar standart oldu.
- **GitHub Sponsors badge'i** — `c792b67` commit'inden beri header'da; FUNDING.yml ile birlikte gelir.
- **D-Terminal latest release link'i** — header'da öne çıkarılır (en aktif/canlı projemiz). Latest projeyi temsil eden link periyodik güncellenebilir.
- **D Brand Family kart sayısı: 8** — yeni repo eklendiğinde kart eklenir. Bu kart yapısı diğer 7 D Brand repolarının "D Brand Ailesi" bölümleriyle senkron tutulmalı.
- **Çöp dosyaları (`CTempd-*-readme.md`)** — diğer repolar için draftların kazara buraya yazılmış halleri. Düzenli temizlik gerekir.
