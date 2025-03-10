In the /app folder you might’ve seen “globals.css” that is a .css file.

---

Next.js provides several ways, of CSS in your application including: 

- [CSS Modules](https://nextjs.org/docs/app/getting-started/css#css-modules)
- [Global CSS](https://nextjs.org/docs/app/getting-started/css#global-css)
- [Tailwind CSS](https://nextjs.org/docs/app/getting-started/css#tailwind-css)
- [Sass](https://nextjs.org/docs/app/getting-started/css#sass)
- [CSS-in-JS](https://nextjs.org/docs/app/getting-started/css#css-in-js)
- [External Stylesheets](https://nextjs.org/docs/app/getting-started/css#external-stylesheets)

This will guide you through how to use each of these approaches

---

## CSS Modules

CSS Modules locally scope CSS by generating unique class names; This allows you to use the same class in different files without worrying about collisions.

To start using CSS Modules, create a new file with the extension `.module.css` and import it into any component inside the `app` directory:

```css
/* app/blog/styles.module.css */
.blog {
  padding: 24px;
}
```

```tsx
// app/blog/page.tsx
import styles from './styles.module.css'
 
export default function Page({ children }: { children: React.ReactNode }) {
  return <main className={styles.blog}>{children}</main>
}
```

---
