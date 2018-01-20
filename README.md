# TODO: Work on the name.

![Visualization]()

### Motivation

### Goals

- Abstract the differences between environments on all necessary levels:
    - Architecture
    - Resources
    - Operating System
- Simply reuse existing code and test files. All prior tests should be ok.
- Easy to both write and run, tests meant only to run on a real IoT device.

### Decisions & Defenses

- `Ansible` is utilized to facilitate build and deployment of code to the desired physical IoT targets.
    - *Why?* `Ansible` leverages ssh to do it's thing, this project assumes ssh access is available on the IoT target.
- Why `Golang`, specifically for IoT development?
    - Footprint
    - Cross-compile support, and ease.
    - Ginkgo shoutout.
    - Static or dynamic linking for your IoT situation.
- Why build tests as a runnable?
    - Both `ginkgo`, and thereby `go test` support it.
    - Leverage dev machine resources.
    - Simple to build for target IoT architecture.
