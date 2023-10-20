# The Buildbarn project

The Buildbarn project provides an implementation of the
[Remote Execution protocol](https://github.com/bazelbuild/remote-apis).
This protocol is used by tools such as [Bazel](https://bazel.build/),
[Buck2](https://buck2.build/),
[BuildStream](https://wiki.gnome.org/Projects/BuildStream/) and
[recc](https://gitlab.com/bloomberg/recc) to cache and optionally
execute build actions remotely.

# Repository guide

In [bb-deployments](https://github.com/buildbarn/bb-deployments) you will find
example configurations for a full Buildbarn deployment. 

You can then have a look at [bb-storage](https://github.com/buildbarn/bb-storage)
to see the implementation of the storage daemon. Buildbarns components takes
only one parameter, the path to a configuration file. The schema for the
configuration files are described in `.proto` format and in the
[proto files](https://github.com/buildbarn/bb-storage/tree/master/pkg/proto/configuration)
you will find detailed descriptions for all of the options.

With [bb-storage](https://github.com/buildbarn/bb-storage) you can configure
a load balanced remote cache solution for your builds after which you can then
move on to [bb-remote-execution](https://github.com/buildbarn/bb-remote-execution)
and find the programs required for remote execution.

As your build grows large you can then set up a
[bb-clientd](https://github.com/buildbarn/bb-clientd) daemon on your workstation.
This is an implementation of the
[remote output service](https://github.com/bazelbuild/bazel/pull/12823/) based
on Buildbarns storage implementation.

# Join us on Slack!

There is a [#buildbarn channel on buildteamworld.slack.com](https://bit.ly/2SG1amT)
that you can join to get in touch with other people who use and hack on
Buildbarn.

# Commercial Support

Buildbarn has an active and enthusiastic community. Though we try to help and
support those who have issues or questions, sometimes organisations need more
dedicated support. The following is a list of community members who you can
contact if you require commercial support. Please submit a PR if you wish to
have your name listed here. Having a name listed is not necessarily an
endorsement.

- [Finn Ball](mailto:finn.ball@codificasolutions.com) - Freelance Consultant
- [Fredrik Medley](mailto:fredrik@meroton.com) - Consultant

## Commercial Hosting and Professional Services

[Meroton](https://www.meroton.com/services/) - Cloud Hosted Buildbarn and Services

Buildbarn does not encourage commercial forks and is willing to engage with
organisations to merge changes upstream in order to be maintained by the
community.
