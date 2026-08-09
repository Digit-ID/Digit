# Publicar o portal Digit no GitHub Pages

1. Cria o repositório `Digit-ID/Digit` (público).
2. Copia para lá os 4 ficheiros desta pasta:
   - `index.html` (o portal, autossuficiente)
   - `manifest.webmanifest`
   - `icon-192.png`
   - `icon-512.png`
3. Em Settings → Pages, ativa "Deploy from a branch" → `main` → `/ (root)`.
4. O portal fica em **https://digit-id.github.io/Digit/**.

## Vantagens de estar em digit-id.github.io
- A sessão Supabase fica no MESMO domínio das 3 apps → login único verdadeiro
  (entras no portal e o DigiNote/DigiSpot/DigiEduca reconhecem a sessão nativamente).
- Instalável como app (PWA) no telemóvel e desktop, com atalhos para as 3 apps.

## Supabase — 2 passos opcionais
- **Foto de perfil**: cria um bucket público chamado `avatars` (Storage → New bucket,
  marca "Public"). Sem ele, a foto fica guardada nos metadados da conta (também funciona).
- **Recuperação de password**: em Authentication → URL Configuration, adiciona
  `https://digit-id.github.io/Digit/` aos Redirect URLs.

## Depois de publicar
Força `Ctrl+Shift+R` — a cache do GitHub Pages é persistente.
