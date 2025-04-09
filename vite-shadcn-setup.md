# Vite / ShadCN Project
### 1. Create Project

```bash
$ npm create vite@latest

> npx
> cva

│
◇  Project name:
│  vite-project-shadcn
│
◇  Select a framework:
│  React
│
◇  Select a variant:
│  TypeScript
│
◇  Scaffolding project in /home/lbravo/workspace-others/vite-project-shadcn...
│
└  Done. Now run:

  cd vite-project-shadcn
  npm install
  npm run dev
```
### 2. Add tailwind CSS
```bash
npm install tailwindcss @tailwindcss/vite
```
### 3. Replace src/index.css with:
```
@import "tailwindcss";
```
### 4. Add the next code to tsconfig.json:
```json
"compilerOptions": {
  "baseUrl": ".",
  "paths": {
    "@/*": [
      "./src/*"
    ]
  }
}
```
### 5. Add the next code to tsconfig.app.json (inside of compilerOptions):
```json
    "baseUrl": ".",
    "paths": {
      "@/*": [
        "./src/*"
      ]
    }
```
### 6. Update vite.config.ts
```bash
npm install -D @types/node
```
```typescript
import path from "path"
import tailwindcss from "@tailwindcss/vite"
import react from "@vitejs/plugin-react"
import { defineConfig } from "vite"

// https://vite.dev/config/
export default defineConfig({
  plugins: [react(), tailwindcss()],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src"),
    },
  },
})
```
### 7. Add Shadcn
```bash
npx shadcn@latest init
```
### 8. Add components
```bash
npx shadcn@latest add button
```
-------------------------------------------

### Add Sass and its integration with Vite
```bash
npm install -D sass
```
