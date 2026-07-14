# Configuration & Real-World Usage

# TS 5 Updates

## Simple Explanation

TypeScript 5 introduced improvements that make development faster, cleaner, and easier. Most of the updates improve performance and add better support for modern JavaScript.

Some useful improvements include: - Faster compilation - Better decorators support - Improved type checking - Better editor support

You don't have to memorize every update. Just make sure you're using the latest stable version.

Check your version:

``` bash
tsc -v
```

# TS Configuration

## Simple Explanation

A TypeScript project is configured using a file called **tsconfig.json**. It tells TypeScript how to compile your project.

Create a configuration file:

``` bash
tsc --init
```

Example

``` json
{
  "compilerOptions": {
    "target": "ES2020",
    "module": "CommonJS",
    "strict": true,
    "outDir": "./dist"
  }
}
```

Common options

-   `target` → JavaScript version to generate
-   `module` → Module system
-   `strict` → Enables strict type checking
-   `outDir` → Output folder for compiled files

# TS with Node.js

## Simple Explanation

TypeScript works very well with Node.js. Instead of writing JavaScript directly, you write TypeScript and compile it into JavaScript.

Install dependencies

``` bash
npm install typescript ts-node @types/node --save-dev
```

Example

``` typescript
function greet(name: string) {
    console.log("Hello " + name);
}

greet("Deepthi");
```

Output

    Hello Deepthi

Run using ts-node

``` bash
npx ts-node app.ts
```

# TS with React

## Simple Explanation

React projects can also be written using TypeScript.

Instead of `.jsx` files, React uses:

    .ts
    .tsx

Example Component

``` tsx
type Props = {
    name: string;
};

function Welcome({ name }: Props) {
    return <h1>Hello {name}</h1>;
}

export default Welcome;
```

Usage

``` tsx
<Welcome name="Deepthi" />
```

Output

    Hello Deepthi

Why use TypeScript with React?

-   Better autocomplete
-   Fewer runtime errors
-   Easier refactoring
-   Better developer experience

# TS Tooling

## Simple Explanation

Tooling means the software that helps us write, check, format, and run TypeScript code.

Common Tools

### VS Code

Provides:

-   Autocomplete
-   Error highlighting
-   Quick fixes

### ESLint

Finds coding mistakes.

Install

``` bash
npm install eslint --save-dev
```

### Prettier

Formats code automatically.

Install

``` bash
npm install prettier --save-dev
```

### ts-node

Runs TypeScript without compiling manually.

``` bash
npx ts-node app.ts
```

Output

Runs the TypeScript file directly.

# Quick Revision

-   TypeScript 5 improves performance and developer experience.
-   `tsconfig.json` controls how TypeScript compiles your project.
-   TypeScript works seamlessly with Node.js.
-   React projects commonly use `.tsx` files.
-   VS Code, ESLint, Prettier, and ts-node make development easier.
