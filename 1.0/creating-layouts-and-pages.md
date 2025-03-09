### **What are layouts??**:

- Layouts are components that define the structure and design shared across pages, in the app.
- Layouts also help making the page have a consistent look, and feel.

### What do layouts do:

- By using layouts, you avoid code dupes, and it ensures that headers, footers and sidebars are consistently rendered across different pages.

## Creating a root layout.

The root layout is defined at the top of your application and it wraps all pages, it **must** include `<html>` and `<body>` tags 

### Example:

```tsx
// app/layout.js
export default function RootLayout({ children }) {
  return (
    <html>
      <body>
        {children}
      </body>
    </html>
  );
}
```

and if you put in the app/page.tsx file:

```tsx
export default function Home() {
  return (
    <div>
      bazinga
    </div>
  );
}
```

when you go onto the website using `npm run dev` it will show the word ‘bazinga’ on the website

## Nested layouts

Nested Layouts are layouts specific to certain sections of your application, for example a dashboard layout can be defined to wrap all of dashboard- related pages

```tsx
// app/dashboard/layout.js
export default function DashboardLayout({ children }) {
  return (
    <div>
      <nav>Dashboard Navigation</nav>
      {children}
    </div>
  );
}
```

## Pages

- **Definition**: Pages are the individual views of your application, represented by files in the **`app`** directory. Each page corresponds to a route in your application.
- **Creating a page:** To create a page, add a `page.js` file in the desired directory

**Example:**

```tsx
// app/about/page.js
export default function AboutPage() {
  return <div>About Us</div>;
}
```

### **Linking Between Pages**

- **Using the Link Component**: Next.js provides a **`Link`** component for client-side navigation between pages. This component enhances performance by prefetching linked pages.

### **Example:**

```tsx
import Link from 'next/link';

export default function HomePage() {
  return (
    <div>
      <h1>Welcome to My Site</h1>
      <Link href="/about">Go to About Page</Link>
    </div>
  );
}
```

# Other stuff:

### **Dynamic Routes**

- **Dynamic Routing**: Next.js supports dynamic routes, allowing you to create pages based on URL parameters. This is useful for pages like product details or user profiles.

### **Metadata in Layouts and Pages**

- **Defining Metadata**: You can define metadata for each page or layout, which is crucial for SEO and sharing on social media.

### **Error Handling in Layouts**

- **Error Boundaries**: You can create error handling components to manage errors at different levels of your application, ensuring a better user experience.

Understanding layouts and pages in Next.js is crucial for building scalable, maintainable applications. Layouts help create a consistent user experience while making page management more efficient. For detailed examples and advanced features, consult the official Next.js documentation and community resources.
