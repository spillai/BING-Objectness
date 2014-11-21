#Do not include files (from libraries) with a main function to avoid conflict 
#with the main function in the project.
add_library(liblinear SHARED linear.cpp tron.cpp)
pods_install_libraries(liblinear)
add_library(blas SHARED blas/daxpy.c blas/ddot.c blas/dnrm2.c blas/dscal.c)
pods_install_libraries(blas)
