https://swr.vercel.app/docs/typescript#generics

If you want to add types for other options of SWR, you can also import those types directly:

```javascript
import useSWR from 'swr'
import type { SWRConfiguration } from 'swr'

const config: SWRConfiguration = {
  fallbackData: "fallback",
  revalidateOnMount: false
  // ...
}

const { data } = useSWR<string[]>('/api/data', fetcher, config)
```
