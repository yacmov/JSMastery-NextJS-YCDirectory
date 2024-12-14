# Project name

## Table of contents

- [Purpose](#purpose)
- [What did I learn with this project?](#what-did-i-learn-with-this-project)
- [Used Programs](#used-programs)
- [References](#reference)

## Purpose

[Back](#table-of-contents)<br>

TODO:

## What did I learn with this project?

[Back](#table-of-contents)<br>

TODO #1:

## Used programs

### ReactJS

### NextJS

### TailwindCSS

- Tailwindcss-animate

```sh
npm install tailwindcss-animate --save
```

```js
import animate from "tailwindcss-animate";
```

- Tailwind-typography

```sh
npm install @tailwindcss/typography --save
```

```js
import typography from "@tailwindcss/typography";
```

### Add into plugins

```js
...
plugins: [animate, typography]
```

Back

### Auth.jsx

[Back](#table-of-contents)<br>

Official site: [Auth.jsx](https://authjs.dev/getting-started/installation)

### Installation

```sh
npm install next-auth@beta
npx auth secret
```

### Create .auth.jsx file

```sh
touch auth.jsx
```

### Add following content

```js
import NextAuth from "next-auth";

export const { handlers, signIn, signOut, auth } = NextAuth({
  providers: [],
});
```

### Create app/api/auth/[...nextauth] folder and route.jsx file in the created folder

```sh
mkdir -p "app/api/auth/[...nextauth]"
touch "app/api/auth/[...nextauth]/route.jsx"
```

### Add following contents

```sh
import { handlers } from "@/auth" // Referring to the auth.ts we just created
export const { GET, POST } = handlers
```

### Authentication: [OAuth](https://authjs.dev/getting-started/authentication/oauth)

Setup with [GitHub](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app)

- Add GitHub Client ID into .env.local

```sh
AUTH_GITHUB_ID="[CLIENT ID]"
```

- Add GitHub Secret ID into .env.local

```sh
AUTH_GITHUB_SECRET="[SECRET ID]"
```

### Updating contents auth.jsx

```js
import NextAuth from "next-auth";
import GitHub from "next-auth/providers/github";

export const { handlers, signIn, signOut, auth } = NextAuth({
  providers: [GitHub],
});
```

## Folder Structure

[Back](#table-of-contents)<br>

### Setup (root) folder

```sh
# Create root 'app/(root)' folder

mkdir -p 'app/(root)'

# Move root `page.jsx` into app/(root) folder

mv 'app/page.jsx' 'app/(root)/'

# Create root layout file into app/(root)

touch 'app/(root)/layout.jsx'
```

### Setup components folder

```sh
# Create components folder

mkdir -p 'app/components'

# Create Navbar.jsx

touch 'app/components/Navbar.jsx'
```

## Reference

[Back](#table-of-contents)<br>

JSMastery
YC_Directory GitHub
