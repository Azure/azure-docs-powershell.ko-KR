---
title: Azure PowerShell cmdlet 출력 형식 지정
description: Azure powershell cmdlet 출력의 형식을 지정 하는 방법.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: e5c9a9df830f6d866d171107472ff94166442be9
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370385"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="6e31d-103">Azure PowerShell cmdlet 출력 형식 지정</span><span class="sxs-lookup"><span data-stu-id="6e31d-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="6e31d-104">기본값으로 각 Azure PowerShell cmdlet은 쉽게 읽을 수 있도록 출력 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="6e31d-105">PowerShell을 사용하면 다음 cmdlet 중 하나로 파이핑하여 cmdlet 출력을 변환하거나 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="6e31d-106">서식 지정</span><span class="sxs-lookup"><span data-stu-id="6e31d-106">Formatting</span></span>      | <span data-ttu-id="6e31d-107">변환</span><span class="sxs-lookup"><span data-stu-id="6e31d-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="6e31d-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="6e31d-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="6e31d-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="6e31d-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="6e31d-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="6e31d-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="6e31d-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="6e31d-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="6e31d-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="6e31d-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="6e31d-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="6e31d-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="6e31d-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="6e31d-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="6e31d-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="6e31d-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="6e31d-116">형식 지정은 PowerShell 터미널에서 표시하는 데 사용되며 전환은 다른 스크립트나 프로그램에서 사용할 데이터를 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="6e31d-117">테이블 출력 형식</span><span class="sxs-lookup"><span data-stu-id="6e31d-117">Table output format</span></span>

<span data-ttu-id="6e31d-118">기본값으로 Azure PowerShell cmdlet 출력은 테이블 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="6e31d-119">이 형식은 요청된 리소스의 모든 정보를 표시하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="6e31d-120">`Format-Table`로 표시되는 데이터 양은 PowerShell 세션 창 너비에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="6e31d-121">특정 속성으로 출력을 제한하고 순서를 지정하려면 속성 이름을 `Format-Table`에 대한 인수로 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="6e31d-122">목록 출력 형식</span><span class="sxs-lookup"><span data-stu-id="6e31d-122">List output format</span></span>

<span data-ttu-id="6e31d-123">목록 출력 형식은 두 개의 열, 속성 이름 뒤에 값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="6e31d-124">복합 개체의 경우 개체의 형식이 대신 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="6e31d-125">다음 출력의 일부 필드가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="6e31d-126">`Format-Table`과 같이 출력을 정렬하고 제한하기 위해 속성 이름을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="6e31d-127">와이드 출력 형식</span><span class="sxs-lookup"><span data-stu-id="6e31d-127">Wide output format</span></span>

<span data-ttu-id="6e31d-128">와이드 출력 형식은 쿼리 당 하나의 속성 이름만 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="6e31d-129">표시되는 속성은 속성을 인수로 제공하여 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="6e31d-130">사용자 지정 출력 형식</span><span class="sxs-lookup"><span data-stu-id="6e31d-130">Custom output format</span></span>

<span data-ttu-id="6e31d-131">`Custom-Format` 출력 형식은 사용자 지정 개체의 형식을 지정하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="6e31d-132">인수가 없으면 `Format-List`처럼 동작하지만 사용자 지정 클래스의 속성 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="6e31d-133">다음 출력의 일부 필드가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="6e31d-134">`Custom-Format`에 대한 인수로 속성 이름을 지정하면 사용자 지정 개체에 대한 속성/값 쌍을 값으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="6e31d-135">다음 출력의 일부 필드가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="6e31d-136">다른 데이터 형식으로 변환</span><span class="sxs-lookup"><span data-stu-id="6e31d-136">Conversion to other data formats</span></span>

<span data-ttu-id="6e31d-137">`ConvertTo-*` cmdlet 제품군을 사용하면 Azure PowerShell cmdlet의 결과를 컴퓨터가 읽을 수 있는 형식으로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="6e31d-138">Azure PowerShell 결과에서 일부 속성만 가져오려면 변환을 수행하기 전에 파이프에서 `Select-Object` 명령을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6e31d-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="6e31d-139">다음 예제는 각 변환이 생성하는 다양한 종류의 출력을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="6e31d-140">CSV로 변환</span><span class="sxs-lookup"><span data-stu-id="6e31d-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="6e31d-141">JSON으로 변환</span><span class="sxs-lookup"><span data-stu-id="6e31d-141">Conversion to JSON</span></span>

<span data-ttu-id="6e31d-142">JSON 출력은 기본값으로 모든 속성을 확장하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="6e31d-143">확장 속성의 깊이를 변경하려면 `-Depth` 인수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="6e31d-144">기본적으로 확장 깊이는 `2`입니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="6e31d-145">다음 출력의 일부 필드가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="6e31d-146">XML로 변환</span><span class="sxs-lookup"><span data-stu-id="6e31d-146">Conversion to XML</span></span>

<span data-ttu-id="6e31d-147">`ConvertTo-XML` cmdlet은 Azure PowerShell 응답 개체를 PowerShell 내의 다른 XML 개체처럼 처리할 수 있는 순수 XML 개체로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="6e31d-148">HTML로 변환</span><span class="sxs-lookup"><span data-stu-id="6e31d-148">Conversion to HTML</span></span>

<span data-ttu-id="6e31d-149">개체를 HTML로 변환하면 HTML 테이블로 렌더링되는 출력이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="6e31d-150">HTML 렌더링은 너비 정보가 없는 표를 렌더링하는 브라우저 동작에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="6e31d-151">사용자 지정 클래스 개체는 확장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e31d-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```
