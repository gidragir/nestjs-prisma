# NestJS + Prisma Fast Deployment Template

High-performance, lightweight boilerplate for NestJS applications. Optimized for **2024+ standards** using **ESNext**, **pnpm**, and **SWC**.

---

## Key Features

* **Modern Runtime**: Configured for **ES2024** and **Node.js 20+**.
* **Ultra-fast Compilation**: Powered by **SWC** (replacing the default `tsc`).
* **Next-gen Tooling**: **Biome** replaces both ESLint and Prettier for 10x faster linting and formatting.
* **Optimized Package Management**: Built with **pnpm** for speed and disk space efficiency.
* **Clean Slate**: All default testing overhead (Jest, Supertest) has been removed for a minimal footprint.

---

## Technical Configuration

### 1. Compiler Strategy (SWC)

To achieve maximum development speed, the project uses the SWC builder.

**Installation:**

```bash
pnpm i --save-dev @swc/cli @swc/core

```

**nest-cli.json:**

```json
{
  "compilerOptions": {
    "builder": "swc",
    "typeCheck": true,
    "deleteOutDir": true
  }
}

```

### 2. TypeScript Environment

The configuration utilizes modern module resolution and target features.

**tsconfig.json:**

```json
{
  "compilerOptions": {
    "module": "ESNext",
    "moduleResolution": "bundler",
    "target": "ES2024"
  }
}

```

### 3. Standards & Formatting (Biome)

Legacy tools (ESLint/Prettier) are replaced with **Biome**.

**Usage:**

```bash
pnpm biome check --write

```
