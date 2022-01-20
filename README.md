Steps to reproduce:

- Create a fresh Next.js app `yarn create next-app whatever`
- Configure a locale in the `i18n` settings in `next.config.js`, for example add `en`
- Start the server (dev or prod, doesn't matter)
- Open an asset under `/_next/`
- Prefix the URL with one of the configured locales
- The exact file doesn't matter, you can even just go to a non-existing URL like `/en/_next/whatever` 
- Watch memory consumption grow rapidly until the server crashes.

> $ yarn next info

```
Operating System:
  Platform: win32
  Arch: x64
  Version: Windows 10 Pro
Binaries:
  Node: 16.13.0
  npm: 8.1.0
  Yarn: 1.22.5
  pnpm: 6.7.3
Relevant packages:
  next: 12.0.8
  react: 17.0.2
  react-dom: 17.0.2
```
