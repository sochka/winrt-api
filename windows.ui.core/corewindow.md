---
-api-id: T:Windows.UI.Core.CoreWindow
-api-type: winrt class
---

<!-- Class syntax.
public class CoreWindow : Windows.UI.Core.ICorePointerRedirector, Windows.UI.Core.ICoreWindow, Windows.UI.Core.ICoreWindow2, Windows.UI.Core.ICoreWindow3, Windows.UI.Core.ICoreWindow4
-->

# Windows.UI.Core.CoreWindow

## -description
Represents the Windows Store app with input events and basic user interface behaviors.

## -remarks
New instances of this class are obtained by calling [CoreApplication.CreateNewView](../windows.applicationmodel.core/coreapplication_createnewview.md) and then inspecting the [CoreWindow](../windows.applicationmodel.core/coreapplicationview_corewindow.md) property on the returned [CoreApplicationView](../windows.applicationmodel.core/coreapplicationview.md) instance. Or you can obtain existing [CoreWindow](corewindow.md) instances for a running app from the [CoreApplication.Views](../windows.applicationmodel.core/coreapplication_views.md) property, or by calling [CoreWindow.GetForCurrentThread](corewindow_getforcurrentthread.md), as seen in the following example.



```cpp
void MyCoreWindowEvents::Run() // this is an implementation of IFrameworkView::Run() used to show context
{
    CoreWindow::GetForCurrentThread()->Activate();

    /...

    CoreWindow::GetForCurrentThread()->Dispatcher->ProcessEvents(CoreProcessEventsOption::ProcessUntilQuit);
}
```



> [!NOTE]
> : This class is not agile, which means that you need to consider its threading model and marshaling behavior. For more info, see [Threading and Marshaling (C++/CX)](http://go.microsoft.com/fwlink/p/?linkid=258275).

## -examples

## -see-also
[CoreApplicationView](../windows.applicationmodel.core/coreapplicationview.md), [CoreApplication.CreateNewView](../windows.applicationmodel.core/coreapplication_createnewview.md), [CoreApplication.Views](../windows.applicationmodel.core/coreapplication_views.md), [Direct2D custom image effects sample (Windows 10)](http://go.microsoft.com/fwlink/p/?LinkId=620531)