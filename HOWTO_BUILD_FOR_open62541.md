Howto build libcheck for open62541
==================================

1. Open a (Visual Studio 2017) Developer Command Prompt
2. cd check_cloned_repo
3. md build
4. cd build
5. cmake -G "NMake Makefiles" -DCMAKE_BUILD_TYPE=RelWithDebInfo -DCMAKE_INSTALL_PREFIX=../install_dir -DCMAKE_C_FLAGS_DEBUG="/MTd" ..
6. nmake
7. nmake install
8. xcopy src\CMakeFiles\check.dir\check.pdb ..\install_dir\lib
9. xcopy lib\CMakeFiles\compat.dir\compat.pdb ..\install_dir\lib

Then rename the install_dir folder to `check`, ZIP it and upload it as a release into the git repo.