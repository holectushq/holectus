# Holectus

**Document collection infrastructure for developers.**

Add document collection to your project in minutes — plug-n-play React components, a typed client, and webhooks against the hosted Holectus API.

Client SDKs (`@holectus/core`, `@holectus/react`, `@holectus/next`) are MIT on npm.

SDK and docs are ready; hosted product access is invite-only while we prepare a wider launch.

## Install

```bash
npm install @holectus/react @holectus/core @holectus/next
```

## Quickstart

1. Create an API key in the Holectus dashboard.
2. Add a Next.js session route with `createHolectusSessionRoute` from `@holectus/next`.
3. Mount `DocumentChecklist` (subject uploads) or `DocumentManager` (admin review).

```tsx
import { DocumentChecklist } from '@holectus/react';
import '@holectus/react/styles.css';

export function SubjectDocuments({ subjectId }: { subjectId: string }) {
  return (
    <DocumentChecklist
      tokenEndpoint={`/api/holectus/session?subjectId=${encodeURIComponent(subjectId)}`}
    />
  );
}
```

## Learn more

- **Docs** — https://docs.holectus.com
- **npm** — [`@holectus/react`](https://www.npmjs.com/package/@holectus/react), [`@holectus/core`](https://www.npmjs.com/package/@holectus/core), [`@holectus/next`](https://www.npmjs.com/package/@holectus/next)

## License

Published SDK packages are MIT. See [LICENSE](./LICENSE).
