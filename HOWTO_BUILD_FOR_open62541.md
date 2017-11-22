Howto build libcheck for open62541
==================================

1. Open a (Visual Studio 2017) Developer Command Prompt
2. cd check_cloned_repo
3. md build
4. cd build
5. cmake -G "NMake Makefiles" -DCMAKE_BUILD_TYPE=RelWithDebInfo -DCMAKE_INSTALL_PREFIX=../install_dir ..
6. nmake
7. nmake install

Then rename the install_dir folder to `check`, ZIP it and upload it as a release into the git repo.