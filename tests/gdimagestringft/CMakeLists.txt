SET(TESTS_FILES
	gdimagestringft_bbox
)

FOREACH(test_name ${TESTS_FILES})
	add_executable(${test_name} "${test_name}.c")
	target_link_libraries (${test_name} ${GDTESTS_TARGET_LINK})
	get_target_property(test_path ${test_name} LOCATION)
	ADD_TEST(${test_name} ${test_path})
ENDFOREACH(test_name)
