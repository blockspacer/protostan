# protostan

The goal of <b>protostan</b> is to provide an API for 
[Stan](github.com/stan-dev/stan) based solely on passing 
(and returning) [protobuf](https://developers.google.com/protocol-buffers/docs/overview)
messages.  The advantages of this approach are:

- As long as a language has protobuf (version 3) support, a
  Stan interface can be written using solely the language and
  its protobuf package without the need to interface with C++.
- Protobuf has [impressive](https://developers.google.com/protocol-buffers/docs/reference/other?hl=en) 
  multi-language support, with apparent priority given to the 
  C++ interface among others.  Other languages important to Stan
  (e.g.-R, Python) also have solid support.
- Protobuf deals with [strongly-typed
  data](https://developers.google.com/protocol-buffers/docs/proto3)
  and offers well-defined mappings from those types to different
  language-specific types.  

We would like to wrap enough of the API so that a first interface
for a language could be written using protobuf without touching
the C++ API.  For the time being this repository should contain:

- Stan-related .proto files for other projects.
- Versions of Stan external API functions with only protobuf 
  messages as input and output types.

Location of Protocol Buffer Message Definitions
===============================================

Message definitions are found in the ``proto`` subdirectory.


Quickstart
==========

1. This repository does not build by itself but as part of the
sakrejda/stan-dev repo.  Clone repository, do NOT clone or build
sub-modules.

```
cd ${DEV_DIR}
git clone https://github.com/sakrejda/stan-dev.git
cd stan-dev
```

2. Set option to build protostan and any missing dependencies.
   By default this includes all the required dependencies.

```
...... HOW?
```

3. Set up a build environment and build.

```
cd ${BUILD_DIR}
cmake ${DEV_DIR}/stan-dev 
make
```

4. Run tests
```
cd ${BUILD_DIR}
ctest
```
 
5. Installation, currently none.



