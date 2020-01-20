# power-sqs-cli

[![Greenkeeper badge](https://badges.greenkeeper.io/singhs020/power-sqs-cli.svg)](https://greenkeeper.io/)

Perform sink operations from power-sqs via cli

## how to install
```javascript
npm install power-sqs-cli -g
```

## how to use

```shell
psqs sinktosqs --source <sourceSQSUrl> --dest <destinationSQSUrl> --stopOnEmpty
```

The *stopOnEmpty* option will close the connection after 5 attempts to read message. If the consecutive attempts return no messages found, the connection will be closed from the source SQS. To keep it running as continous process, please dont use this option.

## power-sqs (Underlying package)
[power-sqs](https://www.npmjs.com/package/power-sqs) can be used as a library as well and provide other functions to perform operations on AWS SQS