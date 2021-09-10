# TPP-container-definitions

Some (hopefully) useful definition files for builing the Trans Proteomic Pipeline inside a container. So far I am only working with Singularity, but the files should be easily adapted to Docker.

## Why?

I don't always use the Trans Proteomic Pipeline as an end-to-end solution, but I do often want to use the tools that are part of it. This can be sometimes be difficult because many tools are not available outisde the TPP and I don't always want to compile the whole thing. So I decided to compile the code in a Singularity container and move the final binaries to a second, slimmer container without all the build dependencies.

## Building a container with the TPP binaries:

1. If you don't already have it on your system, install Singularity: https://sylabs.io/guides/3.8/user-guide/quick_start.html
2. Download the definition file above (e.g. tpp_v6.0.0.def)
3. Build a container like this: `singularity build ./tpp ./tpp.def` where ./tpp is the new container and ./tpp.def is the downloaded definition file.
     - It'll take a while to finish...
