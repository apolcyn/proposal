Ruby Fork Support
----
* Author(s): apolcyn
* Approver: a11r
* Status: Draft
* Implemented in: ruby
* Last updated: July 7th, 2023
* Discussion at: <google group thread> (filled after thread exists)

## Abstract

Provide add a mechanism whereby gRPC-Ruby can be used in a parent process, subsequently forked, and then used again in the child without an exec.

## Background

Currently, gRPC-Ruby does not support forking after the gRPC-Ruby library has been initialized, so applications must defer use of gRPC-Ruby until after any possible forking has been done. This does not work with common forking architectures, for example whereby warmed up worker processes are forked for additional parallelism, while leveraging prior setup.

### Related Proposals: 
* A list of proposals this proposal builds on or supersedes.

## Proposal

[A precise statement of the proposed change.]

### Temporary environment variable protection

[Name the environment variable(s) used to enable/disable the feature(s) this proposal introduces and their default(s).  Generally, features that are enabled by I/O should include this type of control until they have passed some testing criteria, which should also be detailed here.  This section may be omitted if there are none.]

## Rationale

[A discussion of alternate approaches and the trade offs, advantages, and disadvantages of the specified approach.]


## Implementation

[A description of the steps in the implementation, who will do them, and when.  If a particular language is going to get the implementation first, this section should list the proposed order.]

## Open issues (if applicable)

[A discussion of issues relating to this proposal for which the author does not know the solution. This section may be omitted if there are none.]
