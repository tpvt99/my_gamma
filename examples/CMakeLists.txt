set (CMAKE_CXX_STANDARD 11)

include_directories(${GAMMA_SOURCE_DIR}/src)

#add_executable(predictor prediction/AgentInfo.cpp prediction/LearnBounds.cpp prediction/Predict.cpp prediction/WorldBelief.cpp)

add_executable(love prediction/AgentInfo.cpp prediction/LearnBounds.cpp prediction/Predict.cpp prediction/WorldBelief.cpp)
target_link_libraries(love GAMMA pybind11::embed stdc++fs yaml-cpp)

pybind11_add_module(pygamma prediction/AgentInfo.cpp prediction/LearnBounds.cpp prediction/Predict.cpp prediction/WorldBelief.cpp)
target_link_libraries(pygamma GAMMA pybind11::embed stdc++fs yaml-cpp)

#target_link_libraries(predictor GAMMA)
#add_test(predictor predictor)


