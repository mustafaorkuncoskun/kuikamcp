# kuika-tools — Kurulum (lisanslı)

**Gereksinim:** Node.js v20+ · git · geliştiriciden aldığın **lisans anahtarı**.

## İlk kurulum
```
git clone https://github.com/mustafaorkuncoskun/kuikamcp.git
cd kuikamcp
npm install --omit=dev
```
Sonra bu klasörde bir **`.env`** oluştur:  `KUIKA_LICENSE=<sana verilen anahtar>`

MCP'yi aracına ekle (`<yol>` = bu klasörün tam yolu):
- Claude Code: `claude mcp add --scope user kuika-tools -- node "<yol>/dist/index.js"`
- Codex (`~/.codex/config.toml`):
  ```toml
  [mcp_servers.kuika-tools]
  command = "node"
  args = ["<yol>/dist/index.js"]
  ```
Aracı yeniden başlat. İlk Kuika komutunda tarayıcı açılır → kendi Kuika hesabına gir.

## Güncelleme (yeni sürüm uyarısı görünce)
```
git pull
npm install --omit=dev
```

Anahtar yoksa/iptalse araç açılmaz. Sorun olursa geliştiriciye yaz.
