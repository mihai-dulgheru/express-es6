# Enable ES6 syntax in NodeJS and ExpressJS projects

## Steps to run

1. Install dependencies

   ```bash
   npm install
   ```

2. Run the project

   ```bash
   npm start
   ```

## Steps to convert ES5 to ES6

1. Add the following to the package.json file

   ```json
   "type": "module"
   ```

2. Specify the extension when importing local files

   ```javascript
   import { add } from './utils.js';
   ```

3. Replace the `__dirname` variable with the following

   ```javascript
   import { dirname } from 'path';
   import { fileURLToPath } from 'url';

   const __filename = fileURLToPath(import.meta.url);
   const __dirname = dirname(__filename);
   ```

4. Replace the `module.exports` with the following

   ```javascript
   // module.exports = app;
   export default app;
   ```

5. Replace the `require` with the following

   ```javascript
   // const express = require('express');
   import express from 'express';

   // const { join } = require('path');
   import { join } from 'path';
   ```

## Format all files with Prettier

```bash
npx prettier . --write
```
