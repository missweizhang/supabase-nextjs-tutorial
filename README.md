# Supabase NextJS Tutorial

https://supabase.com/docs/guides/getting-started/tutorials/with-nextjs

## Fix: Dynamic server error upon `npm run build`

add this line to any component that uses `cookies`

```
export const dynamic = 'force-dynamic';
```

## Fix: Redirect URL
Replace `http://localhost:3000` in redirect URLs in the codebase with `${location.origin}`.
If you get the error `ReferenceError: location is not defined`, fix the hydration error using [Josh Comeau's solution](https://www.joshwcomeau.com/react/the-perils-of-rehydration/#the-solution-9).

## Javascript client reference

https://supabase.com/docs/reference/javascript/

