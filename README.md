# cpp-bazel-clang-gtest

Enable `clangd` follow 
https://github.com/hedronvision/bazel-compile-commands-extractor#vscode

Make sure to install
 - Bazel https://bazel.build/install/ubuntu#install-on-ubuntu
 - VScode extension
 1. bazel-stack-vscode: https://marketplace.visualstudio.com/items?itemName=StackBuild.bazel-stack-vscode
 1. clangd with configuration

```
"clangd.arguments": [
    "--header-insertion=never",
    "--compile-commands-dir=${workspaceFolder}/",
    "--query-driver=**"
]
```

`bazel run @hedron_compile_commands//:refresh_all`

Other reference:
1. https://github.com/hedronvision/bazel-compile-commands-extractor
1. https://github.com/bazelembedded/rules_cc_toolchain
1. https://bazel.build/docs/bazel-and-cpp
