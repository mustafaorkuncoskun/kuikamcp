# kuika-tools — Kurulum (lisanslı)

**Gereksinim:** Node.js v20+ · geliştiriciden aldığın **lisans anahtarı**.

1) `npm install --omit=dev`
2) Bu klasörde `.env` oluştur:  `KUIKA_LICENSE=<anahtarın>`
3) MCP ekle (`<yol>` = bu klasörün tam yolu):
   - Claude Code: `claude mcp add --scope user kuika-tools -- node "<yol>/dist/index.js"`
   - Codex (`~/.codex/config.toml`):
     ```toml
     [mcp_servers.kuika-tools]
     command = "node"
     args = ["<yol>/dist/index.js"]
     ```
4) Aracı yeniden başlat. İlk komutta tarayıcı açılır → kendi Kuika hesabına gir.

Anahtar yoksa/iptalse araç açılmaz. Sorun olursa geliştiriciye yaz.
