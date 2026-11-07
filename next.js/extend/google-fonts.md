# Extend with Google Fonts

## Configuration

**Refer:** `./src/lib/fonts.ts`

```ts
import {
  Plus_Jakarta_Sans as FontSansHeading,
  Poppins as FontSans,
  Delius as FontSerif,
} from 'next/font/google'

export const fontSansHeading = FontSansHeading({
  subsets: ['latin'],
  weight: ['700', '800'],
  variable: '--font-sans-heading',
})

export const fontSans = FontSans({
  subsets: ['latin'],
  weight: ['400', '500', '600', '700'],
  variable: '--font-sans',
})

export const fontSerif = FontSerif({
  subsets: ['latin'],
  weight: ['400'],
  variable: '--font-serif',
})
```

<!--
@theme {
  --font-sans-heading: 'Plus Jakarta Sans', 'Plus Jakarta Sans Fallback';
  --font-serif: 'Delius', 'Delius Fallback';
}
-->

<!--
{
  source: "/google-fonts/:path*",
  destination: "https://fonts.googleapis.com/:path*",
},
-->

<!--
Dynamic Font Loading

https://github.com/vercel/next.js/discussions/51358
https://borstch.com/snippet/dynamic-font-loading-with-nextjs-14
https://github.com/vercel/next.js/discussions/40345
https://seeratawan.me/blog/lazy-load-fonts-in-nextjs-with-web-components
https://stackoverflow.com/questions/71266063/nextjs-loading-font-from-database
-->

## Issues

### TBD

```log
⨯ Failed to download `Poppins` from Google Fonts. Using fallback font instead.
```

TODO
