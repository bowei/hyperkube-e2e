# Hyperkube-based testing framework

## Overview

This project is a [hyperkube](TODO)-based end-to-end testing
framework. Many [Kubernetes](TODO) projects are possible to integration test
without the use of a fully working cluster. This framework creates a mock
instance of key pieces of the Kubernetes cluster with minimal system
dependencies.

# Framework

## Dependencies

This framework depends on the following:

* [Docker](TODO) 
* A valid `sudo` session
* Write permissions to `/usr/lib/kublet` on the root file-system. This directory
  will be clobbered during a test run.

The framework attempts to exit as cleanly in all possible cases. Please file an
issue if that is not the case.

## What does this framework provide?

This framework provides the following in a containerized manner:

* etcd service (used by the API server)
* API server
* Addon-manager
* Kubelet

## Who should use this framework?

If your project only relies on the API server and Kubelet, then this may be a
good fit for testing your project. This framework is fully compatible with
travis-ci which was one of the motivations for its creation.

# User guide

# Limitations

