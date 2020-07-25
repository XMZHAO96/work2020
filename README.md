# work2020
最新版本为后标0724的文件夹
*使用方法：imgui：https://github.com/ocornut/imgui
1.下载imgui文件
2.下载本链接文件
3.把本链接文件在imgui-master/examples内解压

*项目工程的解决方案平台选择X64
*基于：DirectX12 
      stb_image
      c++
      VS2019
      
# 最新更新：2020.7.25 23:10日本 东京Tokyo,Japan(时区UTC/GMT +9小时)
已实现功能：主窗口/文件资源管理窗口（子）/图片资源管理窗口（子）

+主窗口：
  可以打开文件/图片资源管理窗口
  
+文件资源管理窗口：
   文件搜索（关键字）
   
+图片资源管理窗口：
   显示多个jpg图片文件。
   显示图片文件时去除了窗口。滚动条等组件（仅显示图片）
   显示gif动态图。
   同时显示多个图片文件。
   图片的缩放。
   图片窗口的操作


--Tips：ImGui的介绍里似乎是能够用ImGui::image单独显示图片控件的，但是试了很多次始终没有找到合适的方法，并且即便单独显示图片，对图像的操作控制仍会比较麻烦，所以我思考为把图片和窗口绑定在一起，把图片平铺填充在窗口后对窗口进行缩放等操作时等同于对图片进行操作。
             为了对窗口进行resize，需要显示resize部件，为此在图片资源管理器中增加了一个可取消显示部件的按钮。取消后仅会显示图片自身。

--Bug：目前显示上的Bug为由于窗口和图片进行了绑定，在把图片加载为纹理时关系非常混乱，所以出现了仅显示最新上载的纹理的bug。这个bug会在7.25工作报告时修正；
