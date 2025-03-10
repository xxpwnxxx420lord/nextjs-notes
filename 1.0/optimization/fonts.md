## Handling static assets:
You can store static files, like images and fonts, under a folder called public in the root directory. Files inside of public can be later referenced by your code starting from the root URL (Uniform Resource Locator)
![image](https://github.com/user-attachments/assets/1b118d62-62b5-4209-b866-03634730b81c)

in next.js you can change the font of the website, [this](https://github.com/xxpwnxxx420lord/nextjs-notes/tree/main/codeexamples/fontexample) is a example if you are stuck and the docs aren’t helping.

---

The next/font module automatically optimizes your fonts and removes external network requests for improved privacy and performance.

It Includes **built-in automatic self hosting** for *any*  font file. Meaning you can optimally load web fonts with no layout shift 

To start using `next/font` import it from `next/font/local` or `next/font/google` , call it as a [function](https://www.w3schools.com/typescript/typescript_functions.php) with the appropriate options, and set the [class name](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) of the element you want to, for example:

```tsx
import { Geist } from 'next/font/google'
 
const geist = Geist({
  subsets: ['latin'],
})
 
export default function Layout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="en" className={geist.className}>
      <body>{children}</body>
    </html>
  )
}
```

## google fonts

You can automatically self-host any google font, fonts are included in the deployment and served from the same domain as your deployment, meaning no requests are sent to google by the browser when the user visits your websites here is another example

```tsx
import { Inter } from 'next/font/google'
 
const inter = Inter({
  subsets: ['latin'],
})
 
export default function Layout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="en" className={inter.className}>
      <body>{children}</body>
    </html>
  )
}
```

next.js suggests for people to use [variable fonts](https://fonts.google.com/variablefonts)

you can set weights for boldness, lightness like this

```tsx
import { Inter } from 'next/font/google'
 
const inter = Inter({
  subsets: ['latin'],
  weight: '700'
})
 
export default function Layout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="en" className={inter.className}>
      <body>{children}</body>
    </html>
  )
}
```

and it would look like this
![image](https://github.com/user-attachments/assets/0d48d9e1-68f3-4697-8083-387cede81b64)


## Local fonts

To use a local font, import your font from `next/font/local` and specify the `src` of your local font file in the [`public` folder](https://nextjs.org/docs/app/getting-started/images-and-fonts#handling-static-assets).

```tsx
import localFont from 'next/font/local'
 
const myFont = localFont({
  src: './my-font.woff2',
})
 
export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <html lang="en" className={myFont.className}>
      <body>{children}</body>
    </html>
  )
}
```

For this example, I'm using a [Minecraft font](https://www.fontspace.com/minecrafter-font-f123510) as my custom font example. so my code looks like this:

```
import localFont from 'next/font/local'
 
const myFont = localFont({
  src: '../public/Minecraft.ttf',
})
 
export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <html lang="en" className={myFont.className}>
      <body>{children}</body>
    </html>
  )
}
```
and it looks like this
![image](https://github.com/user-attachments/assets/94ff4fdb-585a-4038-8a03-8040f6517bd8)
