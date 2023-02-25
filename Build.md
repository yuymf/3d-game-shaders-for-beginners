There are probably still people who want to run this project on Windows. So I tell you how I tried

It works in VS2022 (msvc v143), so it works in most cases

1. Clone this project and install Panda3D(1.10.9)

   ```
   git clone https://github.com/lettier/3d-game-shaders-for-beginners.git
   ```

2. Open the visual studio

3. Create new c++ empty project

   - project name: whatever you want
   - location: `{cloned directory}\demonstration`
   - check "place solution and project in the same directory"

4. Move to the project directoy`demonstration\src\main.cxx`

5. Add to the project by 'Add Existing File'

6. Open and comment out `main.cxx``#include <unistd.h>`

7. Change "Debug" to "Release" below the menu bar

8. Open up the project configuration pages

9. Change output directory to in the General tab`$(SolutionDir)..\`

10. Add in the Debugging tab -> Environment`PATH=E:\files\GAMES code\Panda3D-1.10.13-x64\bin;%PATH%`

11. Add in the VC++ directory tab -> External include directoies`E:\files\GAMES code\Panda3D-1.10.13-x64\include`

12. Add in the VC++ directories tab -> Library directories`E:\files\GAMES code\Panda3D-1.10.13-x64\lib`

13. Add the path below in the Linker tab -> input -> Additional Dependencies

    ```
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libp3framework.lib
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libpanda.lib
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libpandaexpress.lib
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libp3dtool.lib
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libpandaphysics.lib
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libp3dtoolconfig.lib
    E:\files\GAMES code\Panda3D-1.10.13-x64\lib\libp3openal_audio.lib
    ```

14. Build the project

15. Execute the binary file (.exe) created in `{cloned directory}\demonstration`