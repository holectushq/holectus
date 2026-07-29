# Holectus

**Document collection infrastructure for developers** — a document collection API and React embeds for upload, review, expiry, and renewal inside your product, with signed webhooks.

Add document collection to your project in minutes — plug-n-play React components, a typed client, and webhooks against the hosted Holectus API.

Client SDKs (`@holectus/core`, `@holectus/react`, `@holectus/next`) are MIT on npm.

SDK and docs are ready; hosted product access is invite-only while we prepare a wider launch.

## Install

```bash
npm install @holectus/react @holectus/core
```

On Next.js App Router, also install `@holectus/next` for `createHolectusSessionRoute`.

## Quickstart

1. Create an API key in the Holectus dashboard.
2. Add a **server** session route that mints tokens via `POST /api/auth/token` (Next.js: `createHolectusSessionRoute` from `@holectus/next`).
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

- **Docs** — https://docs.holectus.com (document collection API & React embeds)
- **Quickstart** — https://docs.holectus.com/quickstart (Next.js document upload checklist)
- **React (any framework)** — https://docs.holectus.com/integrations/react
- **Build vs buy** — https://docs.holectus.com/build-vs-buy
- **Product** — https://holectus.com
- **npm** — [`@holectus/react`](https://www.npmjs.com/package/@holectus/react), [`@holectus/core`](https://www.npmjs.com/package/@holectus/core), [`@holectus/next`](https://www.npmjs.com/package/@holectus/next)

## License

Published SDK packages are MIT. See [LICENSE](./LICENSE).
