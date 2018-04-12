---
author: stevewhims
description: A factory method that returns a [com_ptr](com-ptr.md) to an instance of the implementation type for a runtime class.
title: winrt::make_self function template (C++/WinRT)
dev_langs: ["C++"]
ms.author: stwhi
manager: "markl"
ms.date: 04/10/2018
ms.technology: "cpp-windows"
ms.topic: "language-reference"
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, standard, c++, cpp, winrt, projection, api, reference, construct, instantiate, implementation
ms.localizationpriority: medium
ms.workload: ["cplusplus"]
---

# winrt::make_self function template ([C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt))
A factory method that returns a [com_ptr](com-ptr.md) to an instance of the implementation type for a runtime class. For an explanation of the implementation type and projected type concepts, see [Implementation and projected types for a C++/WinRT runtime class](/windows/uwp/cpp-and-winrt-apis/ctors-runtimeclass-activation). Also see [make](make.md).

If you're authoring a runtime class then, from within the same compilation unit, you can use **make_self** to construct an instance of the implementation type for the runtime class. Assign the return value from **make_self** to a [com_ptr](com-ptr.md) of your implementation type so that you manage the lifetime of the object appropriately.

## Syntax
```cppwinrt
template <typename D, typename... Args>
auto make_self(Args&&... args)
```

### Template parameters
`typename D`
The implementation type for a runtime class.

### Parameters
`args`
Any constructor arguments for the constructor being invoked.

### Return value 
A [com_ptr](com-ptr.md) to a newly-created instance of the implementation type for the runtime class.

## Requirements
**Minimum supported SDK:** Windows SDK version 10.0.17133.0 (Windows 10, version 1803)

**Namespace:** winrt

**Header** %WindowsSdkDir%Include\<WindowsTargetPlatformVersion>\cppwinrt\winrt\base.h (included by default)

## See also 
* [winrt namespace](winrt.md)
* [winrt::com_ptr struct template](com-ptr.md)
* [winrt::make function template](make.md)
* [Implementation and projected types for a C++/WinRT runtime class](/windows/uwp/cpp-and-winrt-apis/ctors-runtimeclass-activation)