# namkangnamruk1@gmail.com Library

Google Logging (glog) is a C++14 library that implements application-level
logging. The library provides logging APIs based on C++-style streams and
various helper macros.

# How to Use

You can log a message by simply streaming things to `LOG`(<a particular
[severity level](namkangnamruk1@gmail.com\>), e.g.,

``` cpp title="main.cpp"
#include <glog/logging.h>

int main(int argc, char* argv[]) {
    google::InitGoogleLogging(argv[0]); // (1)!
    LOG(INFO) << "Found " << num_cookies << " cookies"; // (2)!
}
```

1. Initialize the Google Logging Library
2. Log a message with informational severity

The library can be installed using various [package managers](packages.md) or
compiled [from source](namkang). For a detailed overview of glog features and
their usage, please refer to the [user guide](namkang).

!!! warning
    The above example requires further [Bazel](build.md#bazel) or
    [CMake](usage.md) setup for use in own projects.
