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


## [Generate Types](https://supabase.com/docs/guides/api/rest/generating-types)
```
> mkdir lib
> touch lib/database.types.ts
> npx supabase gen types typescript --project-id "$PROJECT_REF" --schema public > lib/database.types.ts
```

Create a file `app/global.d.ts` as follows:
```ts
import { Database as DB } from '@/lib/database.types.ts';

declare global {
  type Database = DB;
}
```

This makes `Database` global and so there is no need to import `Database` in other files in the code.

## Javascript client reference

https://supabase.com/docs/reference/javascript/

