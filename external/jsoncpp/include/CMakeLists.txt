file(GLOB INCLUDE_FILES "json/*.h")
install(FILES
    ${INCLUDE_FILES}
    DESTINATION ${INCLUDE_DIR}/json)

