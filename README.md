- 👋 Hi there, I’m Michal Nowak - an IT Project Manager!

## Links

## VSC

### extensions
- GitLens (view details of your repo i.e. commits history)
- Playwright for VSC
- Prettier

### config
- format code on save --> View -> Command Palette -> type: "user settings" and open -> search: "format on save" -> check: "Editor Format On Save"

### prettier
- exclude files in `.prettierignore`
```
package-lock.json
playwright-report
test-results
```
- set rules `.prettierrc.json`
```
"singleQuote": true
```
- `npx prettier --write .` --> run Prettier


## Playwright

### commands 
- `node -v` --> check the nodejs version
- `npm init playwright@latest` --> new project with Playwright
- `npx playwright codegen 'URL` --> record tests
- `npx playwright test` --> run test without GUI
- `npx playwright test --headed` --> run test with browser GUI
- `npx playwright show-report` --> show report of latest test
- `npm outdated @playwright` --> czech if Playwright should be updated
- `npm i @playwright/test` --> update Playwright
- `npx playwright install` --> update browsers
- `npx @playwright/test` --> verify Playwright version

### config
- enable video on fail
```javascript
use: {
      video: {'retain-on-failure'},
  },
```
- enable Trave Ciewer on fail
```javascript
use: {
      trace: {'retain-on-failure'},
},
```

### snippets
- import:
```typescript
import { text, expect } from '@playwright@test';
```
- test:
```typescript
test('test description', async {( page )} => {
// code
});
```
- describe:
```typescript
test.describe('group description', () => {
// code
});
```

### package.json scripts
- `"test": "npx playwright test",`
- `"test:headed": "xps playwright test --headed"`
- `"test:login:headed": "npm run test/tests/login.spec.ts -- --headed"`
