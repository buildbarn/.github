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

There is a [#buildbarn channel on buildteamworld.slack.com](https://join.slack.com/t/buildteamworld/shared_invite/zt-45d27zp3m-RzYd2VqdIMxzmn_t0TAg~A)
that you can join to get in touch with other people who use and hack on
Buildbarn.

# Buildbarn community events

## 2025-03-20: Buildbarn meetup at Snowflake in San Mateo

Snowflake hosted our very first Buildbarn meetup. Below is a list of
talks that were given.

- "Buildbarn Portal", presented by Trey Ivy: [slides](https://docs.google.com/presentation/d/1RT47sXQBfJ4Su8pSlavkA06G3Ifju8QUG92-ITj1U54/edit?usp=sharing)
- Panel discussion with Alex Eagle, Benjamin Ingberg, Ed Schouten, Richard Woodbury, and Scott Minor: [video](https://www.youtube.com/watch?v=fl71fFb4m00)
- "Bonanza", presented by Ed Schouten: [video](https://www.youtube.com/watch?v=OuFK-Dh9PUM) [slides](https://docs.google.com/presentation/d/1uh6CxvvziQunw55e_bs1Juz3jfaiE-QJVs2DCfeMeTw/edit?usp=sharing)
- "Buildbarn at Snowflake", presented by Zhimin Xiang and Richard Woodbury: [video](https://www.youtube.com/watch?v=r1abzbs3m1s) [slides](https://docs.google.com/presentation/d/1BVcy_C1Rp-lsuoIz7stCiSYrPLpWllUIrmKfMR2G8hQ/edit?usp=sharing)

## 2026-10-13: Buildbarn meetup at Datadog in Amsterdam

Datadog hosted the second Buildbarn meetup. Below is a list of talks
that were given. We are still in the process of gathering slides and
recordings of this event.

- "Buildbarn at Datadog", presented by James Sharpe and Guilhem Charles: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-who-let-the-builds-out.pdf)
- "The Trio: CI, Bazel, and Buildbarn", presented by Eaugene Thomas: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-ci-at-uber.pdf)
- "bb-storage: Making CDC a First-Class Citizen", presented by Benjamin Ingberg: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-cdc.pdf)
- "bb-portal in Action: An Interactive Build Analysis", presented by Isak Stenström and Oscar Falk: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-bb-portal.pdf)
- "Strategies for GPU Workers in Kubernetes", presented by Chris McDonald: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-strategies-for-gpu-workers.pdf)
- "Buildbarn Helm Charts", presented by Jake Newfield and Cesar Vera-Bernal: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-helm-charts.pdf)
- "Using buildbarn/bb-action-router to Support User-Specified Runner Docker Images at the Action Level", presented by Marcin Kosiba: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-bb-action-router.pdf)
- "Caching Analysis Data in Bonanza", presented by Ed Schouten: [slides](https://github.com/buildbarn/.github/blob/main/slides/20261013-bonanza-caching-analysis.pdf)

Furthermore, Joseph Gette has been kind enough to share
[the 3D models of the Buildbarn swag](https://github.com/JSGette/buildbarn_swag)
he handed out at the meetup.

# Presentations at other venues

The main author of Buildbarn has also given some talks about assorted
topics in the past, including:

- 2021-06-24 Build Meetup: [Automatic worker size selection](https://www.youtube.com/watch?v=3eKVBwlAHsk)
- 2023-05-11 NLUUG conference: [Overview and development history](https://www.youtube.com/watch?v=2_AFPEP4Ewg)

The slides of all of these talks have been combined into a
[a single master slide deck](https://github.com/buildbarn/.github/blob/main/slides/buildbarn-master.pdf).

# Commercial Support

Buildbarn has an active and enthusiastic community. Though we try to help and
support those who have issues or questions, sometimes organisations need more
dedicated support. The following is a list of community members who you can
contact if you require commercial support. Please submit a PR if you wish to
have your name listed here. Having a name listed is not necessarily an
endorsement.

- [Fredrik Medley](mailto:fredrik@meroton.com) - Consultant
- [SUE - Cloud Native Solutions](mailto:sales@sue.eu) - Support & Services Company
- [Tweag by Modus Create](https://www.tweag.io/) - Consulting Services

## Commercial Hosting and Professional Services

- [Aspect Build](https://www.aspect.build/managed-buildbarn) - Self-hosted, Managed Buildbarn
- [Hermetiq](https://www.hermetiq.com/managed-buildbarn) - Managed Buildbarn, build analytics and optimization
- [Meroton](https://www.meroton.com/services/) - Cloud Hosted Buildbarn and Services
- [SUE - Cloud Native Solutions](https://sue.eu/services/) - Support & Services Company

Buildbarn does not encourage commercial forks and is willing to engage with
organisations to merge changes upstream in order to be maintained by the
community.
