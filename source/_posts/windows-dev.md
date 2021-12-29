---
title: Windows Development
date: 2020-03-02 16:45:12
categories:
  - app
tags:
  -
toc: true
---

> see `learn-to-code.md`

[Windows Developer Blog -](https://blogs.windows.com/windowsdeveloper/)
[DotNetCurry.com: Learn .NET Core, ASP.NET MVC, C#, Azure DevOps, JavaScript | Tutorials for Beginners and Experienced Developers](https://www.dotnetcurry.com/)

[Developing Desktop applications in .NET | DotNetCurry](https://www.dotnetcurry.com/dotnet/1506/windows-application-dotnet) !important
[Download a Windows 10 virtual machine - Windows app development](https://developer.microsoft.com/en-us/windows/downloads/virtual-machines/) Win10 VM

[Microsoft releases free Windows Apps programming course - gHacks Tech News](https://www.ghacks.net/2015/10/01/microsoft-releases-free-windows-apps-programming-course/)
[Windows 10 development for absolute beginners | Channel 9](https://channel9.msdn.com/Series/Windows-10-development-for-absolute-beginners)
[Windows-Readiness/AbsoluteBeginnersWin10](https://github.com/Windows-Readiness/AbsoluteBeginnersWin10)
[Developer’s Guide to Windows 10 | Channel 9](https://channel9.msdn.com/Events/Windows/Developers-Guide-to-Windows-10-RTM)

[Choose your app platform | Microsoft Docs](https://docs.microsoft.com/en-us/windows/apps/desktop/choose-your-platform)  
[UWP vs. WPF · jbe2277/waf Wiki](https://github.com/jbe2277/waf/wiki/UWP-vs.-WPF)  
[With Project Reunion Microsoft is Attempting to Unify Win32 and UWP APIs](https://www.infoq.com/news/2020/05/microsoft-project-reunion/)  
non-UWP apps are called "desktop apps" in Microsoft parlance

[Hosted App Model - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2020/03/19/hosted-app-model/)

## .NET Runtime

> see `c-sharp.md#.net-runtime`

## Visual Studio

[microsoft/vswhere: Locate Visual Studio 2017 and newer installations](https://github.com/microsoft/vswhere)
[Finding installed Visual C++ tools for Visual Studio 2017 | C++ Team Blog](https://devblogs.microsoft.com/cppblog/finding-the-visual-c-compiler-tools-in-visual-studio-2017/)

[MSBuild - Visual Studio | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild?view=vs-2019)

[Display WPF Trace Information - Visual Studio | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/debugger/how-to-display-wpf-trace-information?view=vs-2019)

## Installer

[Squirrel/Squirrel.Windows: An installation and update framework for Windows desktop apps](https://github.com/Squirrel/Squirrel.Windows)

### Inno Setup

[Inno Setup](https://jrsoftware.org/isinfo.php)
[Inno Setup Help](https://jrsoftware.org/ishelp/)

[Create Software Installer with Inno Setup - YouTube](https://www.youtube.com/watch?v=z5g_79_nD-g)
[Python 101: Episode #44 - Creating an Installer with Inno Setup - YouTube](https://www.youtube.com/watch?v=jPnl5-bQGHI)

### NSIS

[NSIS Wiki](https://nsis.sourceforge.io/Main_Page)
[NSIS Users Manual](https://nsis.sourceforge.io/Docs/)
[Nullsoft Scriptable Install System - Wikiwand](https://www.wikiwand.com/en/Nullsoft_Scriptable_Install_System)

[Using NSIS To Make Installer Packages](https://www2.seas.gwu.edu/~drum/java/lectures/appendix/installer/install.html)

### Windows Installer

[Windows Installer - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/msi/windows-installer-portal)
[Reducing Patch Size - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/msi/reducing-patch-size)

## UI thread

UI thread is of thread ID 1 ([Thread.ManagedThreadId Property (System.Threading)](https://docs.microsoft.com/en-us/dotnet/api/system.threading.thread.managedthreadid?view=net-5.0))
All UI drawing should be called with UI thread

This can be archived with [Dispatcher](https://docs.microsoft.com/en-us/dotnet/api/system.windows.threading.dispatcher?view=net-5.0)

```csharp
public class MessageBoxWrapper
{
    public static MessageBoxResult Show(string msg, string title, MessageBoxButton buttonStyle, MessageBoxImage image)
    {
        var result = MessageBoxResult.None;

        if (Application.Current.Dispatcher.CheckAccess())
        {
            // Determines whether the calling thread is the thread associated with this Dispatcher.
            result = MessageBox.Show(Application.Current.MainWindow, msg, title, buttonStyle, image);
        }
        else
        {
            // Invoke to block the thread until MessageBox is dismissed
            Application.Current.Dispatcher.Invoke(DispatcherPriority.Normal, new Action(() => {
                result = MessageBox.Show(Application.Current.MainWindow, msg, title, buttonStyle, image);
            }));
        }

        return result;
    }
}
```

## UWP

[UWP Documentation - UWP app developer - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/)
[What's a Universal Windows Platform (UWP) app? - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/get-started/universal-application-platform-guide)
[Create a Universal Windows Platform (UWP) App with Visual Studio and C# | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/get-started/csharp/tutorial-uwp?view=vs-2019)
UWP uses .NET Native for release build, which compiles to machine code

[Microsoft .NET - .NET and Universal Windows Platform Development | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2015/windows-10-special-issue/microsoft-net-net-and-universal-windows-platform-development) 2015; custom-build configuration for debugging .NET Native

### API

[Windows UWP Namespaces - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/)
`Windows.UI.Xaml.Controls`
[Windows.UI.Xaml.Controls Namespace - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.controls?view=winrt-18362)

### React Native for Window & Mac

[Blog · React Native for Windows & Mac](https://microsoft.github.io/react-native-windows/blog/)
[microsoft/react-native-windows: A framework for building native Windows apps with React.](https://github.com/Microsoft/react-native-windows)

[Getting Started · React Native for Windows & Mac](https://microsoft.github.io/react-native-windows/docs/getting-started)

### Sample apps/Toolkit

> see `#winui`

[microsoft/Windows-universal-samples: API samples for the Universal Windows Platform.](https://github.com/microsoft/Windows-universal-samples)
[microsoft/WindowsTemplateStudio: Windows Template Studio quickly builds a UWP app, using a wizard-based UI to turn your needs into a foundation of Windows 10 patterns and best practices.](https://github.com/Microsoft/WindowsTemplateStudio/)
[Van Arsdel Sample App Released! - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2019/01/18/van-arsdel-sample-app-released/)

`Microsoft.Toolkit.Uwp.UI`  
[The Windows Community Toolkit - YouTube](https://www.youtube.com/watch?v=wNmzaiuDqtI)
[windows-toolkit/WindowsCommunityToolkit: The Windows Community Toolkit is a collection of helper functions, custom controls, and app services.](https://github.com/windows-toolkit/WindowsCommunityToolkit)
[Windows Community Toolkit Documentation - Windows Community Toolkit | Microsoft Docs](https://docs.microsoft.com/en-us/windows/communitytoolkit/)

`Telerik.UI.for.UniversalWindowsPlatform`  
[Getting Started with Telerik UI for UWP](https://www.telerik.com/blogs/getting-started-with-telerik-ui-for-uwp)
[telerik/UI-For-UWP: This repo contains the source code for Telerik UI for Universal Windows Platform (UWP), which includes 20+ UI controls for developers building UWP applications.](https://github.com/telerik/UI-For-UWP)
[Adaptive UI for building Windows 10 apps - UI for UWP](https://www.telerik.com/universal-windows-platform-ui)
[What's Next for Telerik UI for UWP - YouTube](https://www.youtube.com/watch?v=R7dZ_UpqkPo)

### Runtime

> this seems to be a .NET Native build step used in Visual Studio

UWP runs on .NET Core (and .NET Native)
By adding the meta package `Microsoft.NETCore.UniversalWindowsPlatform`

[dotnet/README.md at master · microsoft/dotnet](https://github.com/Microsoft/dotnet/blob/master/releases/UWP/README.md)

### Web Request

[httpclient](https://docs.microsoft.com/en-us/windows/uwp/networking/httpclient)
[common function](https://blog.zhengzi.me/c_sharp_uwp_http_get_and_post/)
[examples](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/HttpClient/cs)

### Visual Layer

"CSS" of XAML, allows custom draw components
[Visual Layer - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/composition/visual-layer)
[Interop between XAML and the Visual Layer - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2016/08/26/interop-between-xaml-and-the-visual-layer/)
[Animations with the Visual Layer - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2016/09/16/animations-with-the-visual-layer/)

### Background Task

[Guidelines for background tasks - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/launch-resume/guidelines-for-background-tasks)
[Support your app with background tasks - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/launch-resume/support-your-app-with-background-tasks)

In-process and out-of-process variant
Respond to Triggers (like Andriod's Intent)
30s execution time limitation

[Windows-universal-samples/Samples/BackgroundTask at master · microsoft/Windows-universal-samples](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/BackgroundTask)

## WPF

> From a 1000-meter view, you can think of WPF as a rich layer over DirectX and Windows Forms as thinner layer over GDI Plus.

[Windows Presentation Foundation (WPF) for .NET Core documentation | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/?view=netdesktop-5.0)
[What is Windows Presentation Foundation - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop-wpf/overview/)
[Hello World app with WPF in C# - Visual Studio | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/get-started/csharp/tutorial-wpf?view=vs-2019)

[Welcome - The complete WPF tutorial](https://www.wpf-tutorial.com/)
[Top Features Of Windows Presentation Foundation (WPF)](https://www.c-sharpcorner.com/UploadFile/8a67c0/top-features-of-windows-presentation-foundation-wpf/)

[Events - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/wpf/advanced/events-wpf)
[Layout - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/wpf/advanced/layout)
[Styles and templates - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop-wpf/fundamentals/styles-templates-overview)

[dotnet/wpf: WPF is a .NET Core UI framework for building Windows desktop applications.](https://github.com/dotnet/wpf)

[IAmTimCorey - YouTube](https://www.youtube.com/channel/UC-ptWR16ITQyYOglXyQmpzw)
[Intro to WPF: Learn the basics and best practices of WPF for C# - YouTube](https://www.youtube.com/watch?v=gSfMNjWNoX0)

[Graphics rendering overview - WPF .NET Framework | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/graphics-multimedia/wpf-graphics-rendering-overview?view=netframeworkdesktop-4.8)
[3D Graphics Overview - WPF .NET Framework | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/graphics-multimedia/3-d-graphics-overview?view=netframeworkdesktop-4.8)
[Animation Overview - WPF .NET Framework | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/graphics-multimedia/animation-overview?view=netframeworkdesktop-4.8)
[A Critical Deep Dive into the WPF Rendering System | Jer's Hacks](https://jeremiahmorrill.wordpress.com/2011/02/14/a-critical-deep-dive-into-the-wpf-rendering-system/)
[How to: Render on a Per Frame Interval Using CompositionTarget - WPF .NET Framework | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/graphics-multimedia/how-to-render-on-a-per-frame-interval-using-compositiontarget?view=netframeworkdesktop-4.8)

[2,000 Things You Should Know About WPF | Everything a WPF Developer Needs to Know, in Bite-Sized Chunks](https://wpf.2000things.com/)

### API

`Microsoft.Toolkit.Wpf.UI`
[Microsoft.Toolkit.Wpf.UI.Controls Namespace | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/microsoft.toolkit.wpf.ui.controls?view=win-comm-toolkit-dotnet-stable)
`System.Windows.Controls`
[System.Windows.Controls Namespace | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.windows.controls?view=netframework-4.8)

### Navigation

[WPF Navigation](https://paulstovell.com/wpf-navigation/)

[NavigationService Class (System.Windows.Navigation) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.windows.navigation.navigationservice?view=net-5.0)

[NavigationService in MVVM Light V5 | Around and About .NET World](https://marcominerva.wordpress.com/2014/10/10/navigationservice-in-mvvm-light-v5/)

[Everything about implementing Back Navigation In UWP App](https://www.c-sharpcorner.com/UploadFile/909697/everything-about-back-navigation-in-uwp/)

### Virtualization

[Optimize control performance - WPF .NET Framework | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/advanced/optimizing-performance-controls?view=netframeworkdesktop-4.8)
[XAML Anti-Patterns: Virtualization](https://www.codemag.com/article/1407081/XAML-Anti-Patterns-Virtualization)

[VirtualizingStackPanel Class (System.Windows.Controls) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.windows.controls.virtualizingstackpanel)
[ListView Class (System.Windows.Forms) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.windows.forms.listview?view=net-5.0)

### Sample apps/Toolkit

[Material Design In XAML](http://materialdesigninxaml.net/) depends on MahApps.Metro
[MaterialDesignInXAML/MaterialDesignInXamlToolkit: Google's Material Design in XAML & WPF, for C# & VB.Net.](https://github.com/MaterialDesignInXAML/MaterialDesignInXamlToolkit)
[Home · MaterialDesignInXAML/MaterialDesignInXamlToolkit Wiki](https://github.com/MaterialDesignInXAML/MaterialDesignInXamlToolkit/wiki)

[Keboo/MaterialDesignInXaml.Examples: A collection of small samples using MaterialDesignInXaml.](https://github.com/Keboo/MaterialDesignInXaml.Examples)
[Keboo/ShowMeTheXAML: A WPF component making it easy to show the corresponding XAML for WPF custom styles and controls](https://github.com/Keboo/ShowMeTheXAML) required by "Material Design In XAML"
[c# - The name "XamlDisplay" does not exist in the namespace - Stack Overflow](https://stackoverflow.com/questions/50209200/the-name-xamldisplay-does-not-exist-in-the-namespace)
[C# and WPF - Material Design in Xaml - YouTube](https://www.youtube.com/watch?v=Vrs1VuxGZFw)
[Material Design In XAML Toolkit An Introduction - YouTube](https://www.youtube.com/watch?v=-n5yeEOsbCk)

[MahApps.Metro Documentation](https://mahapps.com/)
[MahApps/MahApps.Metro: A framework that allows developers to cobble together a better UI for their own WPF applications with minimal effort.](https://github.com/MahApps/MahApps.Metro)

[firstfloorsoftware/mui: Modern UI for WPF](https://github.com/firstfloorsoftware/mui)

[samples/wpf at master · dotnet/samples](https://github.com/dotnet/samples/tree/master/wpf)

### UWP features in WPF apps

[Modernize your desktop apps for Windows | Microsoft Docs](https://docs.microsoft.com/en-us/windows/apps/desktop/modernize/)

[Desktop Applications with XAML. Part 2: Desktop Bridge – csharp.christiannagel.com](https://csharp.christiannagel.com/2018/10/09/desktopbridge/) use WinRT API

[Modernizing Desktop Apps on Windows 10 with .NET Core 3.0 and much more | Microsoft Build 2018 | Channel 9](https://channel9.msdn.com/events/Build/2018/BRK3501)
[Desktop Applications with XAML. Part 3: XAML Islands – csharp.christiannagel.com](https://csharp.christiannagel.com/2018/11/06/xamlisland/)

[UWP controls in desktop apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/apps/desktop/modernize/xaml-islands) XAML islands
[XAML Islands - A deep dive - Part 1 - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2018/11/02/xaml-islands-a-deep-dive-part-1/)
[XAML Islands - A deep dive - Part 2 - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2018/11/08/xaml-islands-a-deep-dive-part-2/)
[windows-toolkit/Microsoft.Toolkit.Win32: This repository contains all controls for WPF and WinForms to simplify and demonstrate usage of UWP controls](https://github.com/windows-toolkit/Microsoft.Toolkit.Win32)

[How to Bring Your Classic Desktop App to the New Millennium](https://www.telerik.com/blogs/uwp-wpf-winforms-desktop-app-to-the-new-millennium-with-xaml-islands)
[Getting Started with XAML Islands: Host UWP Control in WPF](https://www.telerik.com/blogs/getting-started-xaml-islands-hosting-uwp-control-in-wpf-winforms-apps)
[Getting Started with XAML Islands: Host UWP Control in WPF](https://www.telerik.com/blogs/getting-started-xaml-islands-hosting-uwp-control-in-wpf-winforms-apps)

[Modernize your desktop app using the Visual layer | Microsoft Docs](https://docs.microsoft.com/en-us/windows/apps/desktop/modernize/visual-layer-in-desktop-apps)
[Using the Visual Layer with WPF | Microsoft Docs](https://docs.microsoft.com/en-us/windows/apps/desktop/modernize/using-the-visual-layer-with-wpf)

## Winforms

[dotnet/winforms: Windows Forms is a .NET Core UI framework for building Windows desktop applications.](https://github.com/dotnet/winforms) .NET wrapper around Win32 API

## WinUI

Windows UI Library, controls and Fluent styles for applications. WinUI 3 aims to be framework independent.

[UWP toolkits - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/toolkits/)

[microsoft/microsoft-ui-xaml: Windows UI Library: the latest Windows 10 native controls and Fluent styles for your applications](https://github.com/microsoft/microsoft-ui-xaml)
[Windows UI Library Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) WinUI2 and WinUI 3
[Windows.UI.Xaml.Controls Namespace - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.controls?view=winrt-19041)

### WinUI 2

`Microsoft.UI.XAML`
[Windows UI library - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/toolkits/winui/)  
[Getting started with the Windows UI library - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/toolkits/winui/getting-started) UWP+WinUI 2

### WinUI 3

[WinUI 3.0 Alpha](https://docs.microsoft.com/en-us/uwp/toolkits/winui3/)  
[microsoft/Xaml-Controls-Gallery at winui3alpha](https://github.com/microsoft/Xaml-Controls-Gallery/tree/winui3alpha)
[Building Modern & Performant Desktop Apps—Is WinUI 3.0 the Way to Go?](https://www.telerik.com/blogs/building-modern-performant-desktop-apps-winui-30-the-way-to-go)  
[_WinUI 3.0 Developer Experience and Tooling - Input Needed_](https://github.com/microsoft/microsoft-ui-xaml/issues/1045)
[How Does .NET 5 Do XAML? By Decoupling It from Windows with WinUI 3, C#/WinRT and More -- Visual Studio Magazine](https://visualstudiomagazine.com/articles/2021/01/11/xaml-net5.aspx)
[WinUI 3 Preview 3 | Windows Dev](https://devblogs.microsoft.com/pax-windows/winui-3-preview-3/)

WinUI 3 expand the scope of WinUI to include the full Windows 10 native UI platform, which will now be fully decoupled from the UWP SDK.  
So WinUI 3 + WPF ≈ UWP windows PC application

To start using WinUI 3.0 developers must:

1. Add the WinUI reference to their solution
2. Update all names spaces in code behind to use the latest Microsoft.\*(Windows.UI-->Microsoft.UI)
3. Update control references to ensure WinUI controls and not SDK controls are being loaded
4. Test and verify

### Fluent Design

[Fluent Design for Windows](https://www.microsoft.com/design/fluent/#/windows)
[Design and UI for UWP - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/design/)
[Fluent Design System for Windows | Microsoft Docs](https://docs.microsoft.com/en-us/windows/apps/fluent-design-system)

### XAML

XAML are compiled to .Net code.
UWP uses [WindowsXamlManager Class (Windows.UI.Xaml.Hosting) - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.hosting.windowsxamlmanager?view=winrt-18362)
XAML Island uses [DesktopWindowXamlSource Class (Windows.UI.Xaml.Hosting) - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.hosting.desktopwindowxamlsource?view=winrt-18362)

[XAML platform - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/xaml-platform/)
[Desktop Applications with XAML. Part 1: UWP – csharp.christiannagel.com](https://csharp.christiannagel.com/2018/09/27/xamldesktop1/)

[microsoft/microsoft-ui-xaml: Windows UI Library: the latest Windows 10 native controls and Fluent styles for your applications](https://github.com/microsoft/microsoft-ui-xaml)
[microsoft/Xaml-Controls-Gallery: This app demonstrates the controls available in the Fluent Design System and Xaml.](https://github.com/microsoft/Xaml-Controls-Gallery)
[microsoft/InventorySample: Sample UWP application for LOB scenarios](https://github.com/Microsoft/InventorySample)
[Design and UI for UWP - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/design/)
Tutorials on various controls

[XAML Spy](http://xamlspy.com/download) Express edition is free

[Uno Playground](https://playground.platform.uno/) XAML edit on Web
[XAML overview - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop-wpf/fundamentals/xaml)

[A significant update to the XAML Designer | Visual Studio Blog](https://devblogs.microsoft.com/visualstudio/a-significant-update-to-the-xaml-designer/)

#### Data binding

[Data binding - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/data-binding/)
[Data binding in depth - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/data-binding/data-binding-in-depth)
[Binding markup extension' - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/xaml-platform/binding-markup-extension)
[UWP Basics | Microsoft Press Store](https://www.microsoftpressstore.com/articles/article.aspx?p=2931577&seqNum=2)

[Data binding overview - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop-wpf/data/data-binding-overview)

leave the code behind XAML empty, use MVVM patterns
[xaml - Why to avoid the codebehind in WPF MVVM pattern? - Stack Overflow](https://stackoverflow.com/questions/6421372/why-to-avoid-the-codebehind-in-wpf-mvvm-pattern)

[UWP Binding vs. XBind - CodeProject](https://www.codeproject.com/Articles/1218367/UWP-Binding-vs-XBind)

[Rockford Lhotka - Using the MVVM pattern requires a framework](http://www.lhotka.net/weblog/PermaLink,guid,c61fd797-16f7-4f5f-a6fc-226f235b132a.aspx)
[wpf - How to choose NOT to use a framework (Caliburn.Micro, etc.) in a given MVVM application? - Software Engineering Stack Exchange](https://softwareengineering.stackexchange.com/questions/287322/how-to-choose-not-to-use-a-framework-caliburn-micro-etc-in-a-given-mvvm-appl)
[The Evolving Infrastructure of .NET Core | .NET Blog](https://devblogs.microsoft.com/dotnet/the-evolving-infrastructure-of-net-core/)

Complexity:

- Code behind (not MVVM)
- MVVM Basic (`System.ComponentModel` in .NET Core, lacking in features)
- MVVM Light (good compromise between complexity and features)
- Prism (originally Microsoft Project, not much UWP tutorial, API ranges from simple to advanced)
- Caliburn.Micro (complex and disorientating; too much magic)

[MVVM Pattern Using WPF in Visual Studio 2012](https://www.c-sharpcorner.com/UploadFile/raj1979/mvvm-pattern-using-wpf-in-visual-studio-2012/) `System.ComponentModel`
[Patterns - WPF Apps With The Model-View-ViewModel Design Pattern | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern) implementing `ViewModelBase` from `System.ComponentModel`
[UWP Basics | Microsoft Press Store](https://www.microsoftpressstore.com/articles/article.aspx?p=2931577&seqNum=5)
[UWP Binding vs. XBind - CodeProject](https://www.codeproject.com/Articles/1218367/UWP-Binding-vs-XBind)

[PropertyChangedEventHandler Delegate (System.ComponentModel) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.componentmodel.propertychangedeventhandler?view=netcore-3.1)
[PropertyChangedEventHandler Delegate (Windows.UI.Xaml.Data) - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.data.propertychangedeventhandler?view=winrt-18362)

[MVVM Light Toolkit](http://www.mvvmlight.net/)
[MVVM Light Toolkit - Documentation](http://www.mvvmlight.net/doc)
[Getting Started With MVVM Light With WPF](https://www.c-sharpcorner.com/article/getting-started-with-mvvm-light-with-wpf/)
[WPF MVVM Introduction](http://dotnetpattern.com/wpf-mvvm-introduction)
[Start with Galasoft MVVM Light Toolkit](http://dotnetpattern.com/mvvm-light-introduction)
[MVVM Light Toolkit Example](http://dotnetpattern.com/mvvm-light-toolkit-example)
[MVVM - IOC Containers and MVVM | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2013/february/mvvm-ioc-containers-and-mvvm)
[MVVM - Messenger and View Services in MVVM | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2013/march/mvvm-messenger-and-view-services-in-mvvm)
[MVVM - Maximizing the Visual Designer’s Usage with Design-Time Data | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2013/april/mvvm-maximizing-the-visual-designer%e2%80%99s-usage-with-design-time-data)
[MVVM - Commands, RelayCommands and EventToCommand | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2013/may/mvvm-commands-relaycommands-and-eventtocommand)
[MVVM - Multithreading and Dispatching in MVVM Applications | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2014/april/mvvm-multithreading-and-dispatching-in-mvvm-applications)
[MVVM - The MVVM Light Messenger In-Depth | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2014/june/mvvm-the-mvvm-light-messenger-in-depth)
[MVVM Light – Code Tips](https://sergeytihon.com/2018/04/16/be-better-wpf-mvvmlight-developer-in-2018/#post-5209:~:text=Part%20%232%3A%20MVVM%20Light%20%E2%80%93%20Code%20Tips)

[canton7/Stylet: A very lightweight but powerful ViewModel-First MVVM framework for WPF for .NET Framework and .NET Core, inspired by Caliburn.Micro.](https://github.com/canton7/Stylet)

[ReactiveUI - An advanced, composable, reactive model-view-viewmodel framework](https://reactiveui.net/)
[Building Cross-Platform Reactive .NET Apps - Artyom V. Gorchakov - Medium](https://medium.com/@worldbeater/reactive-ui-fody-cross-platform-forms-7b501d79f46b)
[Reactive MVVM Pattern On The .NET Platform - Artyom V. Gorchakov - Medium](https://medium.com/@worldbeater/reactive-mvvm-for-net-platform-175dc69cfc82)

[Caliburn.Micro · 'Xaml made easy' · Caliburn.Micro](https://caliburnmicro.com/)
[Documentation · Caliburn.Micro](https://caliburnmicro.com/documentation/)

[Introduction to Prism | Prism](https://prismlibrary.com/docs/) uses `BindableBase` as model base class
[PrismLibrary/Prism: Prism is a framework for building loosely coupled, maintainable, and testable XAML applications in WPF, Windows 10 UWP, and Xamarin Forms.](https://github.com/PrismLibrary/Prism)
[Implementing the MVVM Pattern Using the Prism Library for WPF | Prism](https://prismlibrary.com/docs/wpf/legacy/Implementing-MVVM.html)
[Prism: Patterns For Building Composite Applications With WPF | Microsoft Docs](https://docs.microsoft.com/en-us/archive/msdn-magazine/2008/september/prism-patterns-for-building-composite-applications-with-wpf)
[Getting Started: MVVM Pattern Using Prism Library in WPF](https://www.c-sharpcorner.com/article/getting-started-mvvm-pattern-using-prism-library-in-wpf/)
[Essentials Of MVVM 💻📱🖥️](https://www.c-sharpcorner.com/article/essential-of-mvvm/)
[Brian Lagunas - Microsoft Author | Pluralsight](https://www.pluralsight.com/authors/brian-lagunas)

[.NET Flux Toolkit Nuget Announcement – Alex Dunn](https://alexdunn.org/2017/10/07/net-flux-toolkit-nuget-announcement/)
[SuavePirate/FluxToolkit: A super simple library to enable the implementation of Flux in .NET Applications such as Xamarin, UWP, WPF, and more.](https://github.com/SuavePirate/FluxToolkit/)
[The More Things Change - bitquabit](https://www.bitquabit.com/post/the-more-things-change/) React is Windows 1.0

## Media

[NuGet Gallery | FFMpegCore 1.3.3](https://www.nuget.org/packages/FFMpegCore)

[video - DirectShow, Media Foundation, DXVA, what? - Stack Overflow](https://stackoverflow.com/questions/38706914/directshow-media-foundation-dxva-what)
[About Media Foundation - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/medfound/about-the-media-foundation-sdk)

[.NET Core Image Processing | .NET Blog](https://devblogs.microsoft.com/dotnet/net-core-image-processing/)

[ImageSharp Introduction](https://docs.sixlabors.com/articles/imagesharp/index.html?tabs=tabid-1)
[SixLabors/ImageSharp: A modern, cross-platform, 2D Graphics library for .NET](https://github.com/SixLabors/ImageSharp)

[mono/SkiaSharp: SkiaSharp is a cross-platform 2D graphics API for .NET platforms based on Google's Skia Graphics Library. It provides a comprehensive 2D API that can be used across mobile, server and desktop models to render images.](https://github.com/mono/SkiaSharp/)

### FFMpeg

[NuGet Gallery | FFMediaToolkit 2.2.1](https://www.nuget.org/packages/FFMediaToolkit/)
[radek-k/FFMediaToolkit: FFMediaToolkit is a cross-platform video decoder/encoder library for .NET that uses FFmpeg native libraries.](https://github.com/radek-k/FFMediaToolkit) support streams, uses FFmpeg.AutoGen

[Ruslan-B/FFmpeg.AutoGen: FFmpeg auto generated unsafe bindings for C#/.NET and Mono.](https://github.com/Ruslan-B/FFmpeg.AutoGen)

[Accord.Video.FFMPEG Namespace](http://accord-framework.net/docs/html/N_Accord_Video_FFMPEG.htm) support streams
[Extract Frames from Video C# - Stack Overflow](https://stackoverflow.com/questions/35380868/extract-frames-from-video-c-sharp)

CLI builders, for file based transcoding
[rosenbjerg/FFMpegCore: A great way to use FFMpeg encoding when writing video applications, client-side and server-side. It has wrapper methods that allow conversion to all web formats: MP4, OGV, TS and methods of capturing screens from the videos.](https://github.com/rosenbjerg/FFMpegCore)
[AydinAdn/MediaToolkit: A .NET library to convert and process all your video & audio files.](https://github.com/AydinAdn/MediaToolkit)

### Image Rendering

XAML `ImageElement` must happen in UI thread through Dispatcher
All renderings in XAML are asynchronous

```csharp
var task = _imageElement.Dispatcher.RunAsync(CoreDispatcherPriority.Normal,
  async () =>
  {
      with var latestBitmap = getBitmap();
      await imageSource.SetBitmapAsync(latestBitmap);
  }
);
```

[Graphics rendering overview - WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview)

[Windows-universal-samples/Samples/CameraFrames/cs at master · microsoft/Windows-universal-samples · GitHub](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/CameraFrames/cs)
[Use OpenCV with MediaFrameReader - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/audio-video-camera/use-opencv-with-mediaframereader)
[Process media frames with MediaFrameReader - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/audio-video-camera/process-media-frames-with-mediaframereader)

[opencvsharp/BitmapConverter.cs at master · shimat/opencvsharp · GitHub](https://github.com/shimat/opencvsharp/blob/master/src/OpenCvSharp.Extensions/BitmapConverter.cs)

https://stackoverflow.com/questions/21555394/how-to-create-bitmap-from-byte-array
https://docs.microsoft.com/en-us/dotnet/api/system.drawing.bitmap?view=dotnet-plat-ext-3.1
https://docs.microsoft.com/en-us/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1

[BitmapImage Class (Windows.UI.Xaml.Media.Imaging) - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.bitmapimage?view=winrt-18362)

### DirectX Interop

[FallFury - A DirectX/C++/XAML Tutorial | Channel 9](https://channel9.msdn.com/Series/FallFury) 2013
[Direct3D Rendering Cookbook](https://subscription.packtpub.com/book/game_development/9781849697101) 2014

[DirectX graphics and gaming - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/directx)
[DirectX and XAML interop - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/gaming/directx-and-xaml-interop)
[Module 3. Windows Graphics - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/learnwin32/module-3---windows-graphics)
[Direct2D - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct2d/direct2d-portal)
[DirectWrite - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/directwrite/direct-write-portal)
[Avalonia/src/Windows/Avalonia.Direct2D1 at master · AvaloniaUI/Avalonia · GitHub](https://github.com/AvaloniaUI/Avalonia/tree/master/src/Windows/Avalonia.Direct2D1)
[DigitalRune/Source/DigitalRune.Graphics/Interop at master · DigitalRune/DigitalRune · GitHub](https://github.com/DigitalRune/DigitalRune/tree/master/Source/DigitalRune.Graphics/Interop)
[Profiling DirectX Apps - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct2d/profiling-directx-applications)

[Host Direct3D9 content in WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/advanced/walkthrough-hosting-direct3d9-content-in-wpf?view=netframeworkdesktop-4.8)
[WPF and Direct3D9 interop | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/desktop/wpf/advanced/wpf-and-direct3d9-interoperation?view=netframeworkdesktop-4.8)
[D3DImage Class (System.Windows.Interop) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.windows.interop.d3dimage) which is a `System.Windows.Media.ImageSource`
SwapChain is not usable in WPF application, where the framework is doing the presentation

[Introduction to D3DImage - CodeProject](https://www.codeproject.com/Articles/28526/Introduction-to-D3DImage)
[How to render by using a Direct2D device context - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct2d/devices-and-device-contexts) to DX11 runtime
[Surface Sharing Between Windows Graphics APIs - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3darticles/surface-sharing-between-windows-graphics-apis)
[Drawing with Direct2D - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/learnwin32/drawing-with-direct2d)

[c++ - Direct2D window black when not in focus - Stack Overflow](https://stackoverflow.com/questions/2608283/direct2d-window-black-when-not-in-focus)
[Handle device removed scenarios in Direct3D 11 - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/gaming/handling-device-lost-scenarios)

[Home | SharpDX](http://sharpdx.org/)
[sharpdx/SharpDX-Samples: Official repository for all SharpDX Samples](https://github.com/sharpdx/SharpDX-Samples)
[NuGet Gallery | SharpDX.MediaFoundation 4.2.0](https://www.nuget.org/packages/SharpDX.MediaFoundation/)
[Posts tagged SharpDX - Johan Falk](http://www.johanfalk.eu/blog/tag/sharpdx)

[WPF 使用 SharpDx 渲染博客导航](https://blog.lindexi.com/post/WPF-%E4%BD%BF%E7%94%A8-SharpDx-%E6%B8%B2%E6%9F%93%E5%8D%9A%E5%AE%A2%E5%AF%BC%E8%88%AA.html)
[WPF 使用 SharpDX](https://blog.lindexi.com/post/WPF-%E4%BD%BF%E7%94%A8-SharpDX.html) hWnd rendering
[WPF 使用 SharpDX 在 D3DImage 显示](https://blog.lindexi.com/post/WPF-%E4%BD%BF%E7%94%A8-SharpDX-%E5%9C%A8-D3DImage-%E6%98%BE%E7%A4%BA.html#%E7%94%BB%E5%87%BA%E6%9D%A5) Control Rendering
[WPF 使用封装的 SharpDx 控件](https://blog.lindexi.com/post/WPF-%E4%BD%BF%E7%94%A8%E5%B0%81%E8%A3%85%E7%9A%84-SharpDx-%E6%8E%A7%E4%BB%B6.html)

[SlimDX/slimdx: Automatically exported from code.google.com/p/slimdx](https://github.com/SlimDX/slimdx) deprecated
[RichardsSoftware.net - SlimDX DirectX 11 Tutorials](http://richardssoftware.net/Home/DirectX11Tutorials)

[NuGet Gallery | MediaFoundation 3.1.0](https://www.nuget.org/packages/MediaFoundation/)
Originally [Media Foundation .NET](http://mfnet.sourceforge.net/)
[Of Itself So - Tanta, Windows Media Foundation Sample Projects](http://www.ofitselfso.com/Tanta/)
[OfItselfSo/Tanta: This project provides Sample Projects which can assist people in developing applications for Windows Media Foundation in the C# language.](https://github.com/OfItselfSo/Tanta)
[Windows_Media_Foundation_Getting_Started_CSharp.pdf](http://www.ofitselfso.com/Tanta/Windows_Media_Foundation_Getting_Started_CSharp.pdf)

[Windows.Ui.Xaml.Media.Dxinterop.h header - Win32 apps | Microsoft Docs](https://docs.microsoft.com/zh-hk/windows/win32/api/windows.ui.xaml.media.dxinterop/)
[smourier/DirectN: Direct interop Code for .NET : DXGI, WIC, DirectX 9 to 12, Direct2D, Direct Write, Direct Composition, Media Foundation, WASAPI, CodecAPI, GDI, Spatial Audio, DVD, Windows Media Player, UWP DXInterop, etc.](https://github.com/smourier/DirectN)

[microsoft/Win2D: Win2D is an easy-to-use Windows Runtime API for immediate mode 2D graphics rendering with GPU acceleration. It is available to C#, C++ and VB developers writing apps for the Windows Universal Platform (UWP). It utilizes the power of Direct2D, and integrates seamlessly with XAML and CoreWindow.](https://github.com/Microsoft/Win2D)
[Introduction](https://microsoft.github.io/Win2D/html/Introduction.htm)

## Debugging

[UWP App Diagnostics - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2017/06/28/uwp-app-diagnostics)

[Dependency Walker (depends.exe) Home Page](https://www.dependencywalker.com/)

[Debugging WPF Applications - WPF Debugging and Performance Succinctly Ebook](https://www.syncfusion.com/ebooks/wpf_debugging_and_performance/debugging-wpf-applications)

[Fix NonPaged Memory Leak | Poolmon - Windows 10 And Server | Easy Steps » LEARN Inside](https://learn-inside.com/fix-nonpaged-memory-leak-poolmon-windows-server/)
[windows - What are "Commited Memory", "Cached", "Paged", "Not-paged pool" & How They are Different with "In-Use Memory" - Super User](https://superuser.com/questions/1410289/what-are-commited-memory-cached-paged-not-paged-pool-how-they-are-d)
[Huge Memory Usage in Non-Paged Pool in Windows | Windows OS Hub](http://woshub.com/huge-memory-usage-non-paged-pool-windows/)
[PoolMonX/pooltag.txt at master · zodiacon/PoolMonX](https://github.com/zodiacon/PoolMonX/blob/master/res/pooltag.txt)

[Ask The Performance Team - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/ask-the-performance-team/bg-p/AskPerf)
[Fundamentals of garbage collection | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)
[Cleaning up unmanaged resources | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/unmanaged)

[PerfView Tutorial | Channel 9](https://channel9.msdn.com/Series/PerfView-Tutorial)
[microsoft/perfview: PerfView is a CPU and memory performance-analysis tool](https://github.com/Microsoft/perfview)

[Luke Stackwalker home page](http://lukestackwalker.sourceforge.net/) call graph, profiler
[How I cut GTA Online loading times by 70%](https://nee.lv/2021/02/28/How-I-cut-GTA-Online-loading-times-by-70/)

[Download Debug Diagnostic Tool v2 Update 3.1 from Official Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=102635)
[How to Use Debug Diagnostic Tool to Collect Dumps on Hanging or Crashing Process in PowerCenter - YouTube](https://www.youtube.com/watch?v=5MqFlcACSzI)

[c# - Cannot obtain value of local or argument as it is not available at this instruction pointer, possibly because it has been optimized away - Stack Overflow](https://stackoverflow.com/questions/8311303/cannot-obtain-value-of-local-or-argument-as-it-is-not-available-at-this-instruct)

[x64dbg](https://x64dbg.com/#start)
[glmcdona/Process-Dump: Windows tool for dumping malware PE files from memory back to disk for analysis.](https://github.com/glmcdona/Process-Dump)

[WinDbg - Wikiwand](https://www.wikiwand.com/en/WinDbg)
[Download Debugging Tools for Windows - WinDbg - Windows drivers | Microsoft Docs](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugger-download-tools)
[Getting Started with WinDbg (User-Mode) - Windows drivers | Microsoft Docs](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/getting-started-with-windbg)
[Collecting User-Mode Dumps - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/wer/collecting-user-mode-dumps?redirectedfrom=MSDN)

[TsudaKageyu/minhook: The Minimalistic x86/x64 API Hooking Library for Windows](https://github.com/TsudaKageyu/minhook)

## Testing

[dotnet test command - .NET Core CLI | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-test)

[c - Is there a good Valgrind substitute for Windows? - Stack Overflow](https://stackoverflow.com/questions/413477/is-there-a-good-valgrind-substitute-for-windows)

### xUnit

[Home > xUnit.net](https://xunit.net/)
[Getting started: .NET Core with command line > xUnit.net](https://xunit.net/docs/getting-started/netcore/cmdline)
[Getting started: Multi-targeting with non-Windows OSes > xUnit.net](https://xunit.net/docs/getting-started/multi-target/non-windows)

```sh
# target .NET Core, not .NET Standard
dotnet add package xunit xunit.runner.visualstudio
```

Define tests with `[Fact]` attribute

[index at XUnitPatterns.com](http://xunitpatterns.com/index.html)

### NUnit

[NUnit.org](https://nunit.org/)

### MSTest

[microsoft/testfx-docs: Docs for MSTest V2 test framework](https://github.com/Microsoft/testfx-docs)
[Use Microsoft.VisualStudio.TestTools.UnitTesting in unit tests - Visual Studio | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/test/using-microsoft-visualstudio-testtools-unittesting-members-in-unit-tests?view=vs-2019)
[Get started with unit testing - Visual Studio | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/test/getting-started-with-unit-testing?view=vs-2019)

## MSIX

[MSIX documentation - MSIX | Microsoft Docs](https://docs.microsoft.com/en-us/windows/msix/)
[MSIX: Package desktop apps for Windows 10. Replace outdated installers. | Tabs vs Spaces | Channel 9](https://channel9.msdn.com/Shows/Tabs-vs-Spaces/MSIX-Package-desktop-apps-for-Windows-10-Replace-outdated-installers)
[Building an MSIX package from your code overview - MSIX | Microsoft Docs](https://docs.microsoft.com/en-us/windows/msix/desktop/source-code-overview)

[Packaging Universal Windows apps for Windows 10 | Microsoft Docs](<https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh454036(v=vs.140)>)
[Package a desktop app from source code using Visual Studio - MSIX | Microsoft Docs](https://docs.microsoft.com/en-us/windows/msix/desktop/desktop-to-uwp-packaging-dot-net)
[Packaging MSIX apps - MSIX | Microsoft Docs](https://docs.microsoft.com/en-us/windows/msix/package/packaging-uwp-apps)

## WinRT API

[Windows Runtime - Wikiwand](https://www.wikiwand.com/en/Windows_Runtime)
[C++/WinRT - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/)

[Enhancing Non-packaged Desktop Apps using Windows Runtime Components - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2019/04/30/enhancing-non-packaged-desktop-apps-using-windows-runtime-components/)
[Microsoft paves the way to Windows APIs | InfoWorld](https://www.infoworld.com/article/3604655/microsoft-paves-the-way-to-windows-apis.html)

[Using WinML in .NET5 | #ifdef Windows](https://devblogs.microsoft.com/pax-windows/using-winml-in-net5/)

- net5.0-windows10.0.17763.0 (Windows 10, version 1809)
- net5.0-windows10.0.18362.0 (Windows 10, version 1903)
- net5.0-windows10.0.19041.0 (Windows 10, version 2004)

### Rust

[Overview of developing on Windows with Rust | Microsoft Docs](https://docs.microsoft.com/en-us/windows/dev-environment/rust/overview)
[microsoft/windows-rs: Rust for Windows](https://github.com/microsoft/windows-rs)
[Rust for Windows, and the _windows_ crate | Microsoft Docs](https://docs.microsoft.com/en-us/windows/dev-environment/rust/rust-for-windows)
[Build more secure software with Rust for Windows | InfoWorld](https://www.infoworld.com/article/3615991/build-more-secure-software-with-rust-for-windows.html)

## I18n

[Localize strings in your UI and app package manifest - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/app-resources/localize-strings-ui-manifest)
[Use a Custom Resource Markup Extension to Succeed at UI String Globalization! | Windows Dev](https://devblogs.microsoft.com/pax-windows/use-a-custom-resource-markup-extension-to-succeed-at-ui-string-globalization/) better than Uid

## COM

[Win32 and COM APIs for UWP apps - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/uwp/win32-and-com/win32-and-com-for-uwp-apps)

[core-setup/COM-activation.md at master · dotnet/core-setup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/COM-activation.md)
[samples/core/extensions/ExcelDemo at master · dotnet/samples](https://github.com/dotnet/samples/tree/master/core/extensions/ExcelDemo) COM Client
[samples/core/extensions/COMServerDemo at master · dotnet/samples](https://github.com/dotnet/samples/tree/master/core/extensions/COMServerDemo)
