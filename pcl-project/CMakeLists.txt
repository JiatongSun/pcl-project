cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(pcl_project)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (sor_filter sor_filter.cpp)
target_link_libraries (sor_filter ${PCL_LIBRARIES})

add_executable (VGFilter VGFilter.cpp)
target_link_libraries (VGFilter ${PCL_LIBRARIES})

add_executable (passthrough passthrough.cpp)
target_link_libraries (passthrough ${PCL_LIBRARIES})

add_executable (kdtree_search kdtree_search.cpp)
target_link_libraries (kdtree_search ${PCL_LIBRARIES})

add_executable (point_cloud_compression point_cloud_compression.cpp)
target_link_libraries (point_cloud_compression ${PCL_LIBRARIES})

add_executable (filter filter.cpp)
target_link_libraries (filter ${PCL_LIBRARIES})

add_executable (txt_pcd txt_pcd.cpp)
target_link_libraries (txt_pcd ${PCL_LIBRARIES})

add_executable (asc_txt asc_txt.cpp)
target_link_libraries (asc_txt ${PCL_LIBRARIES})

add_executable (cluster_extraction cluster_extraction.cpp)
target_link_libraries (cluster_extraction ${PCL_LIBRARIES})

add_executable (project_inliers project_inliers.cpp)
target_link_libraries (project_inliers ${PCL_LIBRARIES})

add_executable (table_project_inliers table_project_inliers.cpp)
target_link_libraries (table_project_inliers ${PCL_LIBRARIES})

add_executable (bare_earth bare_earth.cpp)
target_link_libraries (bare_earth ${PCL_LIBRARIES})

add_executable (greedy_projection greedy_projection.cpp)
target_link_libraries (greedy_projection ${PCL_LIBRARIES})

add_executable (resampling resampling.cpp)
target_link_libraries (resampling ${PCL_LIBRARIES})

add_executable (concave_hull_2d concave_hull_2d.cpp)
target_link_libraries (concave_hull_2d ${PCL_LIBRARIES})

add_executable (cloud_viewer cloud_viewer.cpp)
target_link_libraries (cloud_viewer ${PCL_LIBRARIES})

