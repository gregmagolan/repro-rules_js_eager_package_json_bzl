```
gregs-mbp:rules_js_eager_package_json_bzl greg$ bazel clean --expunge 2> /dev/null

gregs-mbp:rules_js_eager_package_json_bzl greg$ ls -la $(bazel info output_base)/external
Starting local Bazel server and connecting to it...
ls: /private/var/tmp/_bazel_greg/b2daffd99c5071268d867df32cb119a3/external: No such file or directory

gregs-mbp:rules_js_eager_package_json_bzl greg$ bazel query //...
DEBUG: /private/var/tmp/_bazel_greg/b2daffd99c5071268d867df32cb119a3/external/aspect_rules_js/js/private/js_run_binary.bzl:296:14: 
WARNING: @//:tsc is not configured to produce outputs.

If this is a generated bin from package_json.bzl, consider using the *_binary or *_test variant instead.
See https://github.com/aspect-build/rules_js/tree/main/docs#using-binaries-published-to-npm
//:tsc
//:tsc__entry_point
//:tsc__js_binary
//:tsc_copy_srcs_to_bin
//:tsc_js_filegroup
//:tsc_runfiles
//:tsc_runfiles_lib
Loading: 1 packages loaded

gregs-mbp:rules_js_eager_package_json_bzl greg$ ls -la $(bazel info output_base)/external
total 64
drwxr-xr-x  18 greg  wheel   576 19 Jan 10:51 .
drwxr-xr-x@ 14 greg  wheel   448 19 Jan 10:51 ..
-rw-r--r--   1 greg  wheel   107 19 Jan 10:51 @aspect_bazel_lib.marker
-rw-r--r--   1 greg  wheel   107 19 Jan 10:51 @aspect_rules_js.marker
-rw-r--r--   1 greg  wheel   107 19 Jan 10:51 @bazel_skylib.marker
-rw-r--r--   1 greg  wheel    65 19 Jan 10:51 @bazel_tools.marker
-rw-r--r--   1 greg  wheel    65 19 Jan 10:51 @local_config_platform.marker
-rw-r--r--   1 greg  wheel   281 19 Jan 10:51 @npm.marker
-rw-r--r--   1 greg  wheel   107 19 Jan 10:51 @npm__typescript__4.9.4.marker
-rw-r--r--   1 greg  wheel   107 19 Jan 10:51 @rules_nodejs.marker
drwxr-xr-x  32 greg  wheel  1024 19 Jan 10:51 aspect_bazel_lib
drwxr-xr-x  35 greg  wheel  1120 19 Jan 10:51 aspect_rules_js
drwxr-xr-x  17 greg  wheel   544 19 Jan 10:51 bazel_skylib
lrwxr-xr-x   1 greg  wheel    76 19 Jan 10:51 bazel_tools -> /var/tmp/_bazel_greg/install/cc65259974e62ae1af2ade93d26f6353/embedded_tools
drwxr-xr-x   6 greg  wheel   192 19 Jan 10:51 local_config_platform
drwxr-xr-x   9 greg  wheel   288 19 Jan 10:51 npm
drwxr-xr-x   7 greg  wheel   224 19 Jan 10:51 npm__typescript__4.9.4
drwxr-xr-x   8 greg  wheel   256 19 Jan 10:51 rules_nodejs

gregs-mbp:rules_js_eager_package_json_bzl greg$ ls -la $(bazel info output_base)/external/npm__typescript__4.9.4
total 22728
drwxr-xr-x   7 greg  wheel       224 19 Jan 10:51 .
drwxr-xr-x  18 greg  wheel       576 19 Jan 10:51 ..
-rwxr-xr-x   1 greg  wheel       628 19 Jan 10:51 BUILD.bazel
-rw-r--r--   1 greg  wheel       118 19 Jan 10:51 WORKSPACE
drwxr-xr-x  10 greg  wheel       320 19 Jan 10:51 package
-rw-r--r--   1 greg  wheel  11619457 19 Jan 10:50 package.tgz
-rwxr-xr-x   1 greg  wheel      5183 19 Jan 10:51 package_json.bzl
```