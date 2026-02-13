# ChatGPT Prompt Cheatbook – Next.js & Laravel

Bu depo, **Next.js ve Laravel projeleri için ChatGPT promptları** içeren bir cheatbook olarak tasarlanmıştır.  
Amacı, profesyonel seviye kod standartları, en iyi uygulamalar ve örnekler üzerinden yeni projeler başlatırken referans alınacak bir kaynak sağlamaktır.

---

## 📌 Özellikler
- Next.js projeleri için profesyonel kurallar ve best practice’ler.  
- Laravel projeleri için SOLID ve MVC odaklı rehberler.  
- Kodlama standartları ve isimlendirme konvansiyonları.  
- State yönetimi, UI kütüphaneleri, validasyon, performans ve güvenlik konularında ipuçları.  
- ChatGPT’den hızlıca yararlanarak yeni projeler oluşturmanı kolaylaştırır.

---

## 🗂️ Dosya Yapısı

> **Nextjs PROMPTS.md’ye ulaşmak için tıklayın:** [PROMPTS.md](./nextjs/PROMPTS.md)

> **Larevel PROMPTS.md’ye ulaşmak için tıklayın:** [PROMPTS.md](./laravel/PROMPTS.md)
---

## ⚡ Kullanım
1. PROMPTS.md dosyasındaki kuralları ve örnekleri inceleyin.  
2. ChatGPT’ye bu rehberi referans göstererek yeni Next.js veya Laravel projelerinizi başlatın.  
3. İhtiyaç duydukça yeni prompt örneklerini bu depoya ekleyin.

---

## 🌟 Katkıda Bulunma
Yeni promptlar, en iyi uygulamalar veya güncellemeler eklemek isterseniz, pull request açabilirsiniz.  
Hedefimiz, sürekli güncel ve profesyonel bir cheatbook oluşturmak.


## 💾 Next.js Proje Dump Alma (PowerShell)

Next.js projenizin tüm önemli dosyalarını tek bir metin dosyasında birleştirmek için aşağıdaki PowerShell komutunu kullanabilirsiniz:

```powershell
# Proje kök dizininde çalıştırın
# Tüm TypeScript/JavaScript/CSS/JSON/Markdown dosyalarını tek bir TXT dosyasında birleştirir

Get-ChildItem -Recurse -Include *.ts,*.tsx,*.js,*.jsx,*.json,*.css,*.md |
Where-Object { $_.FullName -notmatch "node_modules|\.next|\.git" } |
ForEach-Object {
    "`n`n===== $($_.FullName) =====`n"  # Dosya başlığı
    [System.IO.File]::ReadAllText($_.FullName, [System.Text.Encoding]::UTF8)  # Dosya içeriği
} | Set-Content nextjs-full-project-dump.txt -Encoding utf8
