# graphql-practice

- *.graphql 에서 import 사용시 ts에서 설정한 path alias 사용 가능 - [@graphql-tools comment](https://github.com/ardatan/graphql-tools/issues/1544#issuecomment-829603999) 참고
  - 결국 apollo-server에서 graphql 파일을 ts로 해석해서 처리하게 됨

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
}
```
