# graphql-practice

*.graphql 에서 import 사용시 ts에서 설정한 path alias 사용 가능 - [@graphql-tools comment](https://github.com/ardatan/graphql-tools/issues/1544#issuecomment-829603999) 참고


```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "experimentalDecorators": true,
    "forceConsistentCasingInFileNames": false,
    "paths": {
      "@common/*": ["../common/*"],
    }
  }
}
```

```graphql
# import "@common/another-types.graphql"

type A {
 field: ImportedType
```
