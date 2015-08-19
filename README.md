# jangle

AWS operations by cli should be simpler

[![PyPI version](https://img.shields.io/pypi/v/jangle.svg)](https://pypi.python.org/pypi/jangle)
[![PyPI downloads](https://img.shields.io/pypi/dm/jangle.svg)](https://pypi.python.org/pypi/jangle)
[![Build Status](https://travis-ci.org/achiku/jangle.svg)](https://travis-ci.org/achiku/jangle)
[![Dependency Status](https://gemnasium.com/achiku/jangle.svg)](https://gemnasium.com/achiku/jangle)


## Description

jangle makes AWS operations simpler and intuitive from your terminal.

## Usage

Listing all EC2 instances

```
jangle ec2 ls
```

Filtering EC2 instances by Name tag

```
jangle ec2 ls *web*
```

Starting instance

```
jangle ec2 up -i i-xxxxxx
```

Stopping instance

```
jangle ec2 down -i i-xxxxxx
```

Listing all ELB instances

```
jangle elb ls
```

Listing a ELB instance

```
jangle elb ls production-blog-elb
```

Listing ELB attached EC2 instances

```
jangle elb ls -l production-blog-elb
```


## Configuration

You can create the credential file yourself. By default, its location is at ```~/.aws/credentials```

```
[default]
aws_access_key_id = YOUR_ACCESS_KEY
aws_secret_access_key = YOUR_SECRET_KEY
```


You may also want to set a default region. This can be done in the configuration file. By default, its location is at ```~/.aws/config```

```
[default]
region = us-east-1
```
