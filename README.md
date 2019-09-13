# xchacha20

XChaCha20 as defined by [the XChaCha20 IRTF CFRG draft](https://tools.ietf.org/html/draft-irtf-cfrg-xchacha-01).

[![Travis](http://img.shields.io/travis/chiefbiiko/xchacha20.svg?style=flat)](http://travis-ci.org/chiefbiiko/xchacha20) [![AppVeyor](https://ci.appveyor.com/api/projects/status/github/chiefbiiko/xchacha20?branch=master&svg=true)](https://ci.appveyor.com/project/chiefbiiko/xchacha20)

## API

``` ts
export const KEY_BYTES: number = 32;
export const NONCE_BYTES: number = 24;

export function xchacha20(
  out: Uint8Array,
  key: Uint8Array,
  nonce: Uint8Array,
  counter: number,
  text: Uint8Array
): void;
```

`xchacha20` does not do any input validation. Make sure `key` and `nonce` have correct sizes and that `counter` is an `uint32`. Also, guarantee that `out.byteLength === text.byteLength`.

## License

[MIT](./LICENSE)