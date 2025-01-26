# electron-shadcn

Electron in all its glory. Everything you will need to develop your beautiful desktop application.

![Demo GIF](https://github.com/LuanRoger/electron-shadcn/blob/main/images/demo.gif)

## Libs and tools

To develop a Electron app, you probably will need some UI, test, formatter, style or other kind of library or framework, so let me install and configure some of them to you.

### Core 🏍️

- [Electron 34](https://www.electronjs.org)
- [Vite 6](https://vitejs.dev)
- [SWC](https://swc.rs)

### DX 🛠️

- [TypeScript 5.7](https://www.typescriptlang.org)
- [Prettier](https://prettier.io)
- [ESLint 9](https://eslint.org)
- [Zod](https://zod.dev)
- [React Query (Tan Stack)](https://react-query.tanstack.com)

### UI 🎨

- [React 19](https://reactjs.org)
- [Tailwind CSS](https://tailwindcss.com)
- [Shadcn UI](https://ui.shadcn.com)
- [Geist](https://vercel.com/font) as default font
- [i18next](https://www.i18next.com)
- [TanStack Router](https://tanstack.com/router)
- [Lucide](https://lucide.dev)

### Test 🧪

- [Jest](https://jestjs.io)
- [Playwright](https://playwright.dev)
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro)

### Packing and distribution 📦

- [Electron Forge](https://www.electronforge.io)

### CI/CD 🚀

- Pre-configured [GitHub Actions workflow](https://github.com/LuanRoger/electron-shadcn/blob/main/.github/workflows/playwright.yml), for test with Playwright

### Project preferences 🎯

- Use Context isolation
- [React Compiler](https://react.dev/learn/react-compiler) is enabled by default.
- `titleBarStyle`: hidden (Using custom title bar)
- Geist as default font
- Some default styles was applied, check the [`styles`](https://github.com/LuanRoger/electron-shadcn/tree/main/src/styles) directory
- React DevTools are installed by default

> If you don't know some of these libraries or tools, I recommend you to check their documentation to understand how they work and how to use them.

## Directory structure

```plaintext
.
└── ./src/
    ├── ./src/assets/
    │   └── ./src/assets/fonts/
    ├── ./src/components/
    │   ├── ./src/components/template
    │   └── ./src/components/ui/
    ├── ./src/helpers/
    │   └── ./src/helpers/ipc/
    ├── ./src/layout/
    ├── ./src/lib/
    ├── ./src/pages/
    ├── ./src/style/
    └── ./src/tests/
```

- `src/`: Main directory
  - `assets/`: Store assets like images, fonts, etc.
  - `components/`: Store UI components
    - `template/`: Store the all not important components used by the template. It doesn't include the `WindowRegion` or the theme toggler, if you want to start an empty project, you can safely delete this directory.
    - `ui/`: Store Shadcn UI components (this is the default direcotry used by Shadcn UI)
  - `helpers/`: Store IPC related functions to be called in the renderer process
    - `ipc/`: Directory to store IPC context and listener functions
      - Some implementations are already done, like `theme` and `window` for the custom title bar
  - `layout/`: Directory to store layout components
  - `lib/`: Store libraries and other utilities
  - `pages/`: Store app's pages
  - `style/`: Store global styles
  - `tests/`: Store tests (from Jest and Playwright)

## NPM script

To run any of those scripts:

```bash
npm run <script>
```

- `start`: Start the app in development mode
- `package`: Package your application into a platform-specific executable bundle and put the result in a folder.
- `make`: Generate platform-specific distributables (e.g. .exe, .dmg, etc) of your application for distribution.
- `publish`: Electron Forge's way of taking the artifacts generated by the `make` command and sending them to a service somewhere for you to distribute or use as updates.
- `lint`: Run ESLint to lint the code
- `format`: Run Prettier to check the code (it doesn't change the code)
- `format:write`: Run Prettier to format the code
- `test`: Run the default unit-test script (Jest)
- `test:watch`: Run the default unit-test script in watch mode (Jest)
- `test:unit`: Run the Jest tests
- `test:e2e`: Run the Playwright tests
- `test:all`: Run all tests (Jest and Playwright)

> The test scripts involving Playwright require the app be builded before running the tests. So, before run the tests, run the `package`, `make` or `publish` script.

## How to use

1. Clone this repository

```bash
git clone https://github.com/LuanRoger/electron-shadcn.git
```

Or use it as a template on GitHub

2. Install dependencies

```bash
npm install
```

3. Run the app

```bash
npm run start
```

## Used by

- [yaste](https://github.com/LuanRoger/yaste) - yaste (Yet another super ₛᵢₘₚₗₑ text editor) is a text editor, that can be used as an alternative to the native text editor of your SO, maybe.
- [eletric-drizzle](https://github.com/LuanRoger/electric-drizzle) - shadcn-ui and Drizzle ORM with Electron.

> Does you've used this template in your project? Add it here and open a PR.

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/LuanRoger/electron-shadcn/blob/main/LICENSE) file for details.
