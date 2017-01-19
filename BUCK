
apple_bundle(
  name = 'TodayExtensionDemo',
  binary = ':TodayExtensionBinary',
  extension = 'app',
  deps = ['//TodayExtension:DemoExtension'],
  info_plist = 'Info.plist',
)

apple_binary(
    name = 'TodayExtensionBinary',
    preprocessor_flags = ['-fobjc-arc'],
    headers = glob([
      '*.h',
    ]),
    srcs = glob([
      '*.m',
    ]),
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
    ],
)
apple_package(
  name = 'TodayExtensionPackage',
  bundle = ':TodayExtensionDemo',
)
