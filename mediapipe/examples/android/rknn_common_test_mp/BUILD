package(default_visibility = ["//visibility:public"])

cc_library(
	name = "rknn_lib",
	srcs = ["librknn_api/arm64-v8a/librknnrt.so"],
	hdrs = ["librknn_api/include/rknn_api.h"],
	strip_include_prefix = "librknn_api/include",
	alwayslink = 1,
)

cc_binary(
	name = "rknn_common_test_mp",
	srcs = ["main.cc"],
	deps=[
        ":rknn_lib",
        "//mediapipe/framework/port:opencv_core",
        "//mediapipe/framework/port:opencv_imgcodecs",
        "//mediapipe/framework/port:opencv_imgproc",
    ]
)