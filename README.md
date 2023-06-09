# Sbt Cats/GraalVM template

A [Giter8][g8] template to bootstrap a Cats/CE3 project that can be compiled to a native image with Docker,
along with some other useful addons such as Scalafix and Scalafmt rules.

## Usage

Create a new project:
```bash
sbt new rzqx/cats.g8
```

Build a native image and then run it with Docker:

```bash
docker build -t cats .
docker run --rm cats
```

As of latest testing, at least ~6GB of memory is required to build the native image. For example, if
running Docker on MacOS, you'll need to allocate at least ~6GB of memory to the Docker VM.

Finally, the Dockerfile provided applies a memory limit of 512MB (`-Xmx512m`) to the native image, which exists
purely for demonstration purposes.

## Template license
Written in 2023 by rzqx <rzqx@pm.me>.

To the extent possible under law, the author(s) have dedicated all copyright and related
and neighboring rights to this template to the public domain worldwide.
This template is distributed without any warranty. See <http://creativecommons.org/publicdomain/zero/1.0/>.

[g8]: http://www.foundweekends.org/giter8/
