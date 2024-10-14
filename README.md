# is-errno-exception
Typescript assertion for Nodejs exceptions

## Instalaton
```sh
npm i --save is-errno-exception
```

## Usage
```ts

import { isErrnoException } from 'is-errno-exception';

try {
  // ...
} catch (e) {
  if (!isErrnoException(e) || e.code !== 'ABORT_ERR') {
    throw e;
  }
  console.log('Aborted');
}

```
