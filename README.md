# Grinta 🔥

> **Grinta** *(italiano: garra, determinação, espírito de luta)*
>
> Multiferramenta de produtividade offline: **Projetos · Conversor · Finanças · Paletas · Timeline · Mapa Mental**

---

## 📦 Stack de Tecnologias

| Camada | Biblioteca | Versão | Para quê |
|--------|-----------|--------|----------|
| **Desktop** | [Electron](https://www.electronjs.org/) | 29 | Janela nativa, menus, IPC |
| **Framework** | [React](https://react.dev/) | 18 | UI reativa |
| **Build** | [Vite](https://vitejs.dev/) | 5 | Dev server rápido + bundler |
| **Estilo** | [Tailwind CSS](https://tailwindcss.com/) | 3 | Utility-first CSS |
| **Animações** | [Framer Motion](https://www.framer.com/motion/) | 11 | Transições spring |
| **Ícones** | [Lucide React](https://lucide.dev/) | latest | 1000+ ícones SVG |
| **Estado global** | [Zustand](https://zustand-demo.pmnd.rs/) | 4 | Store com persist |
| **Gráficos** | [Recharts](https://recharts.org/) | 2 | Gráficos SVG (Finance) |
| **Atalhos** | [react-hotkeys-hook](https://github.com/JohannesKlauss/react-hotkeys-hook) | 4 | Ctrl+K, Ctrl+1-7 |
| **Empacotador** | [electron-builder](https://www.electron.build/) | 24 | .exe, .dmg, .AppImage |

---

## 🚀 Como Rodar

### Pré-requisitos
- **Node.js 18+** → https://nodejs.org

```bash
# Linux / macOS
chmod +x setup.sh && ./setup.sh

# Windows — dê duplo-clique em:
setup.bat

# Ou manualmente:
npm install
npm run dev
```

### Gerar instalador

```bash
npm run dist:win    # → .exe
npm run dist:mac    # → .dmg
npm run dist:linux  # → .AppImage
```

---

## ⌨️ Atalhos

| Atalho | Ação |
|--------|------|
| `Ctrl+K` | Paleta de comandos |
| `Ctrl+1–7` | Abrir módulo direto |
| `F11` | Tela cheia |

---

## 🐙 Como colocar no GitHub

### 1. Criar conta no GitHub
Acesse **github.com** → Sign up → Plano Free

### 2. Instalar Git
- **Windows**: https://git-scm.com/download/win
- **macOS**: `xcode-select --install`
- **Linux**: `sudo apt install git`

### 3. Criar repositório no GitHub
1. Clique **+** → **New repository**
2. Nome: `grinta`
3. **NÃO** marque "Add README" (já temos um)
4. Clique **Create repository**

### 4. Inicializar e enviar

```bash
# Configurar Git (uma vez só)
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"

# Dentro da pasta grinta/
git init
echo "node_modules/\ndist/\nrelease/\n.DS_Store\n*.log" > .gitignore
git add .
git commit -m "feat: Grinta v1.0 — initial release"

# Substitua SEU_USUARIO pelo seu usuário do GitHub
git remote add origin https://github.com/SEU_USUARIO/grinta.git
git branch -M main
git push -u origin main
```

> **Autenticação**: o GitHub vai pedir login. Use seu email + um **Personal Access Token**:
> Settings → Developer settings → Personal access tokens → New token → marque `repo` → Copie o token e use como senha

### 5. Próximos commits

```bash
git add .
git commit -m "feat: descrição da mudança"
git push
```

---

## 📁 Estrutura

```
grinta/
├── electron/main.js + preload.js
├── src/
│   ├── App.jsx
│   ├── store/useAppStore.js   (Zustand)
│   ├── lib/finance|units|colors|utils.js
│   ├── components/layout/ + ui/
│   └── modules/ (7 módulos)
├── vite.config.js + tailwind.config.js
└── setup.sh / setup.bat
```
