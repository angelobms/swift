add_swift_library(swiftCloudKit ${SWIFT_SDK_OVERLAY_LIBRARY_BUILD_TYPES} IS_SDK_OVERLAY
  CKError.swift

  SWIFT_COMPILE_FLAGS "${SWIFT_RUNTIME_SWIFT_COMPILE_FLAGS}"
  LINK_FLAGS "${SWIFT_RUNTIME_SWIFT_LINK_FLAGS}"
  TARGET_SDKS OSX IOS IOS_SIMULATOR TVOS TVOS_SIMULATOR WATCHOS WATCHOS_SIMULATOR
  SWIFT_MODULE_DEPENDS_OSX Darwin Contacts CoreGraphics CoreLocation Dispatch Foundation IOKit ObjectiveC # auto-updated
  SWIFT_MODULE_DEPENDS_IOS Darwin Contacts CoreLocation Dispatch Foundation ObjectiveC # auto-updated
  SWIFT_MODULE_DEPENDS_TVOS Darwin CoreLocation Dispatch Foundation ObjectiveC # auto-updated
  SWIFT_MODULE_DEPENDS_WATCHOS Darwin CoreLocation Dispatch Foundation ObjectiveC # auto-updated
  FRAMEWORK_DEPENDS_WEAK CloudKit
)
