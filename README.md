# ILICIO PS4 Offline Host (`PS4ilicioHost`) — v1.0.0

<p align="center">
  <strong>Host offline para PlayStation 4 desbloqueado, com interface moderna em português (pt-BR), suporte a múltiplos firmwares e integração com GoldHEN.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/versão-1.0.0-4d8eff?style=for-the-badge" alt="Versão 1.0.0">
  <img src="https://img.shields.io/badge/plataforma-PlayStation%204-0b0e17?style=for-the-badge&logo=playstation&logoColor=4d8eff" alt="Plataforma: PlayStation 4">
  <img src="https://img.shields.io/badge/firmware-5.05--13.52-0b0e17?style=for-the-badge&color=34d399" alt="Firmwares: 5.05 a 13.52">
  <img src="https://img.shields.io/badge/idioma-pt--BR-0b0e17?style=for-the-badge&color=4d8eff" alt="Idioma: pt-BR">
</p>

> [!NOTE]
> Este projeto é destinado a fins educacionais, de preservação e pesquisa. Utilize por sua conta e risco. Não possui qualquer afiliação ou endosso da Sony Interactive Entertainment.

---

## Sobre o projeto

O **ILICIO PS4 Offline Host** (`PS4ilicioHost`) é uma coleção estática e autocontida de páginas para desbloqueio de PlayStation 4, projetada para funcionar diretamente no navegador do console tanto online quanto **100% offline** via cache local (`AppCache`).

Na versão **1.0.0**, toda a interface gráfica foi reformulada para um visual moderno inspirado no PlayStation, com foco na legibilidade em TVs, navegação nativa pelo controle (DualShock 4) e tradução completa dos textos explicativos para **pt-BR**, mantendo intactos todos os scripts de exploit e payloads originais.

---

## Firmwares suportados

| # | Firmware | Rota | Fluxo / Exploit | GoldHEN | Payloads utilitários |
|---|---|---|---|---|---|
| 01 | **13.02–13.52** | `1352/index.html` | SlopKit WebKit | `v2.4b18.12` | GoldHEN integrado |
| 02 | **11.00–12.02 / 12.50–13.00** | `1300/index.html` | SlopKit WebKit (Lapse / Poops) | `v2.4b18.12` | GoldHEN integrado |
| 03 | **6.00–11.02** | `css/version-selector.html` | CSSFontFace UAF (Lapse / Poops) | `v2.4b18.12` / `v2.4b18.10` | Menu dedicado de execução |
| 04 | **9.00–9.60** | `900/version-selector.html` | PSFree + Lapse | `v2.4b18.12` / `v2.4b18.10` | Incluídos |
| 05 | **7.00–8.52** | `700/version-selector.html` | PSFree + Lapse | `v2.4b18.12` / `v2.4b18.10` | Incluídos |
| 06 | **6.72** | `672/index.html` | Host dedicado | `v2.4b18.12` / `v2.4b18.10` | Incluídos |
| 07 | **5.05** | `505/index.html` | Host dedicado | `v2.4b18.12` / `v2.4b18.10` | Incluídos |

---

## Como funciona e como usar

1. **Acesse o host no navegador do PS4** (via GitHub Pages ou servidor HTTP local na sua rede).
2. **Escolha o firmware** correspondente ao instalado no seu console no menu principal (`index.html`).
3. **Instalação do cache offline**: Na primeira abertura da rota escolhida, o navegador do PS4 fará automaticamente o download e armazenamento dos arquivos em `AppCache` (exibindo o progresso na tela).
4. **Uso offline**: Após o cache ser concluído, você pode desconectar o PS4 da internet e abrir o navegador novamente — o host carregará instantaneamente direto do cache local.

> [!TIP]
> Se você já utilizava uma versão anterior em cache no PS4, limpe os dados de cache e cookies do navegador do console antes de abrir a versão **1.0.0** para garantir o carregamento da nova interface.

---

## Tecnologias, modelo e ferramentas utilizadas

- **HTML5, CSS3 e JavaScript (Vanilla)**: Construído sem dependências externas ou frameworks pesados, garantindo carregamento rápido e compatibilidade total com as diferentes versões do WebKit presentes nos firmwares do PS4 (incluindo Flexbox `-webkit-flex` para o firmware 5.05).
- **HTML5 Application Cache (`AppCache`)**: Responsável por salvar os arquivos e payloads localmente através dos arquivos `cache.manifest`, `PSPulse.cache` e `PSPulse.manifest`.
- **Antigravity & Gemini**: A reformulação visual da interface, a tradução completa para `pt-BR`, a organização dos arquivos estáticos e a documentação desta versão **1.0.0** foram desenvolvidas com assistência do **Gemini** (modelo **Gemini 4 Hydrogen**) no ambiente **Antigravity**.

---

## Créditos e links

- **Customização e organização (v1.0.0):** [Ilício](https://github.com/Ilicio) — [YouTube (@iliciojr)](https://www.youtube.com/@iliciojr)
- **Base original dos exploits e estrutura:** PSPulse (BlackArch / PlayStation Pulse) e itskenethb (CSSFontFace)
