<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Amazon_Web_Services_Logo.svg/800px-Amazon_Web_Services_Logo.svg.png" alt="AWS" width=200>

A collection of bash shell scripts for automating various tasks with [Amazon Web Services](https://aws.amazon.com/) using the [AWS CLI](https://aws.amazon.com/cli/)

# Introduction

Over the years, I've written a set of utility scripts to automate some of the repetitive and mundane tasks on AWS, thereby avoiding clicks through the AWS web console.  These scripts follow the theme of being simple and requiring only the `jq` utility, and to offer maximum composability where possible.  Some may require more recent versions of bash (i.e. 4.0+).

# Usage

These scripts assume the user has the `AWS_PROFILE` environment variable set.  Some many also assume `AWS_ACCOUNT_ID` and `AWS_ZONE`.  When using something like [direnv](https://direnv.net/), this makes managing multiple projects on multiple accounts very easy, and avoids having to repeatedly type `-p` option, etc.

Many of these scripts have been written with pipe and composability in mind.  See below for some examples:

```
ssh ec2-user@$(aws-ec2-instances | head -1)
```

# Other Projects

This project is highly opinionated.  You may find the following projects more flexible, expansive, or interesting:

* [swoodford/aws](https://github.com/swoodford/aws)

