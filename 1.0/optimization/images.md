# optimizing images

## Handling static assets:

You can store static files, like images and fonts, under a folder called `public` in the root directory. Files inside of public can be later referenced by your code starting from the root URL (Uniform Resource Locator)

## Optimizing images

The next.js `<image>` component extends the html `<tag>` element to provide:

- **Size Optimization**: ****Automatically serving correctly sized images for each device, using modern image formats like [WebP](https://github.com/xxpwnxxx420lord/nextjs-notes/blob/main/1.0/webp-guide.md)
- **Visual stability:** Preventing [layout shift](https://web.dev/articles/cls) automatically when images are loading.
- **Faster page loads:** Only loading images when they enter the viewport using native browser lazy loading, with optional blur-up placeholders.
- **Asset flexibility:** Resizing images on-demand, even images stored on remote servers.

## Local Images

To use a local image, import your `png` `jpg` `webp`  type images to the public folder and run the code.

```tsx
// app/page.tsk
import Image from 'next/image' // this gets the varible <image>
import pic from '../public/name.extension' // dont listen to next.js docs it took me 10 minutes to figure out the mistake in their terrible code.

export default function Page() {
	return (
		 <Image
			 src = {pic}
			 alt="bazinga"
			 // width={500} automatically provided
      // height={500} automatically provided
      // blurDataURL="data:..." automatically provided
      // placeholder="blur" // Optional blur-up while loading	
      />
      )

} 
```

you can read about remote images [here](https://nextjs.org/docs/app/getting-started/images-and-fonts#remote-images)
