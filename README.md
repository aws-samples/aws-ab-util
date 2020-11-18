## AWS AB Util 

AWS AB Util is a utility CLI tool to manage deployment and execution of distributed load test using AB (Apache Bench) using AWS SSM and EC2. It can generate thousands of RPS (Requests per Second) and/or Gigabytes per second of data transfer.

## Requirements
- OS: Linux, MacOS
- Software: [AWS CLI](https://aws.amazon.com/cli/)
- IAM Permissions: AWS SSM Run Command

## Install
```
git clone https://github.com/aws-samples/aws-ab-util.git
mv aws-ab-util/aws-ab-util /usr/local/bin/
rm -fr aws-ab-util
```

## Usage
Overall options.
```
# aws-ab-util
Usage: aws-ab-util <command> [parameters]
  run threads requests url
  create servers_count
  delete
```


Creating 2x load test servers.
```
# aws-ab-util create 2
Creating Load Test Servers...
```


Running a load test with 100 requests, per thread, per server. This will result in 1.000 request (100 requests x 5 threads  x 2 servers).
```
# aws-ab-util run 5 100 https://www.myserver.com/
Running Load Test...
```

Deleting servers
```
# aws-ab-util delete
Deleting Load Test Servers...
```

## Uninstall
```
rm /usr/local/bin/aws-ab-util
```

## SSM Run Command View
![SSM Command Execution](images/aws-ab-command-execution.png)

![SSM Command Output](images/aws-ab-command-output.png)

## Load Test Results Example
![Load test results example](images/aws-ab-load-test.png)

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

