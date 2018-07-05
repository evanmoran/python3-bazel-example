
config_setting(
    name="mac-platform",
    values={"cpu": "darwin"},
    visibility=["//visibility:public"],
)

config_setting(
    name="windows-platform",
    values={"cpu": "x64_windows"},
    visibility=["//visibility:public"],
)

cc_binary(
    name="python3-bazel-example",
    srcs = [
        "main.cc",
    ],
    deps = select({
        ":mac-platform": [
            "@python3//:mac-python-library"
        ],
        ":windows-platform": [
            "@python3//:windows-python-library"
        ]
    })
)