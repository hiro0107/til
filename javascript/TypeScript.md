# TypeScript

es2016を入力に、es5を出力する例
```
{
	"files": [
        "src/main.ts"
    ],
    "compilerOptions": {
        "noImplicitAny": true,
        "target": "es5",
        "lib": ["es2016"]
    }
}
```

参考) https://github.com/Microsoft/TypeScript/issues/11890

# node使用時

```
"moduleResolution": "node"
```
が必要みたい

# WebPackと併用する場合

`.ts` ファイルの解決を書く必要がある

参考) https://stackoverflow.com/questions/43595555/webpack-cant-resolve-typescript-modules
