# bazel-example

Sample bazel app to demonstrate the issue with `rules_nodejs` upgrade to v3.  
See issue: https://github.com/bazelbuild/rules_nodejs/issues/2520

To run the app:
```sh
yarn install
yarn bazel run :bin
```

---

Sample bazel app to demonstrate the usage of Node v16.14.0 in WORKSPACE file
https://github.com/bazelbuild/rules_nodejs/pull/3319
