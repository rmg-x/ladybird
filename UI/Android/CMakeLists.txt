add_library(ladybird SHARED
    src/main/cpp/LadybirdActivity.cpp
    src/main/cpp/WebViewImplementationNative.cpp
    src/main/cpp/WebViewImplementationNativeJNI.cpp
    src/main/cpp/ALooperEventLoopImplementation.cpp
    src/main/cpp/TimerExecutorService.cpp
    src/main/cpp/JNIHelpers.cpp
)
target_link_libraries(ladybird PRIVATE jnigraphics android)

include(../cmake/AndroidExtras.cmake)
create_ladybird_bundle(ladybird)
