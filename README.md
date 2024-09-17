# s3-concat-bundle-issue

This repository is reproduction that issue about s3-concat bundle.

### Build

```sh
npm install
npm run build
```

### Run

```sh
s3-concat-bundle-issue % srcBucketName=<srcBucketName> dstBucketName=<dstBucketName> node index.js
```

terminal output:
```
/Users/fossamagna/git/s3-concat-bundle-issue/node_modules/@aws-sdk/client-s3/dist-cjs/auth/httpAuthSchemeProvider.js:17
        throw new Error(`getEndpointParameterInstructions() is not defined on \`${context.commandName}\``);
              ^

Error: getEndpointParameterInstructions() is not defined on `ListObjectsV2Command`
    at Object.httpAuthSchemeParametersProvider (/Users/fossamagna/git/s3-concat-bundle-issue/node_modules/@aws-sdk/client-s3/dist-cjs/auth/httpAuthSchemeProvider.js:17:15)
    at async /Users/fossamagna/git/s3-concat-bundle-issue/node_modules/@smithy/core/dist-cjs/index.js:61:5
    at async /Users/fossamagna/git/s3-concat-bundle-issue/node_modules/@aws-sdk/middleware-sdk-s3/dist-cjs/index.js:138:14
    at async /Users/fossamagna/git/s3-concat-bundle-issue/node_modules/@aws-sdk/middleware-logger/dist-cjs/index.js:34:22
    at async Ld (/Users/fossamagna/git/s3-concat-bundle-issue/node_modules/s3-concat/dist/s3-concat.umd.cjs:38:15880)
    at async Wd.addFiles (/Users/fossamagna/git/s3-concat-bundle-issue/node_modules/s3-concat/dist/s3-concat.umd.cjs:38:17353)

Node.js v20.11.1
```
