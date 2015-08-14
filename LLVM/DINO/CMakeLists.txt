cmake_minimum_required(VERSION 2.8)

add_llvm_loadable_module(DINO
	DINO.cpp
	DINOTaskSplit.cpp
	DINOTaskCost.cpp
	DINOTaskBoundaries.cpp
	DINOVersioner.cpp
	DINOComplexityAnalysis.cpp
)

if(APPLE)
  set_target_properties(DINO PROPERTIES
    COMPILE_FLAGS "-fno-rtti -fvisibility-inlines-hidden -std=c++11 -stdlib=libc++")
else()
  set_target_properties(DINO PROPERTIES
    COMPILE_FLAGS "-fno-rtti -fvisibility-inlines-hidden -std=c++11")
endif(APPLE)
