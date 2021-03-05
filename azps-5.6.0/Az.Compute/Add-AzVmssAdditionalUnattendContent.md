---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 4f33840ac7716d3e06ddaafe4b5abadab823cfee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981067"
---
# <span data-ttu-id="7bade-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="7bade-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="7bade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bade-102">SYNOPSIS</span></span>
<span data-ttu-id="7bade-103">무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7bade-104">구문</span><span class="sxs-lookup"><span data-stu-id="7bade-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bade-105">설명</span><span class="sxs-lookup"><span data-stu-id="7bade-105">DESCRIPTION</span></span>
<span data-ttu-id="7bade-106">**Add-AzVmssAdditionalUnattendContent** cmdlet은 무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7bade-107">예제</span><span class="sxs-lookup"><span data-stu-id="7bade-107">EXAMPLES</span></span>

### <span data-ttu-id="7bade-108">예제 1: 무인 Windows 설치 응답 파일에 정보 추가</span><span class="sxs-lookup"><span data-stu-id="7bade-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="7bade-109">이 명령은 무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7bade-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7bade-110">PARAMETERS</span></span>

### <span data-ttu-id="7bade-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="7bade-111">-ComponentName</span></span>
<span data-ttu-id="7bade-112">추가된 콘텐츠로 구성할 구성 요소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="7bade-113">유일한 허용되는 값은 Microsoft-Windows-Shell-Setup입니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-114">-Content</span><span class="sxs-lookup"><span data-stu-id="7bade-114">-Content</span></span>
<span data-ttu-id="7bade-115">지정된 경로 및 구성 요소에 대한 unattend.xml 추가되는 XML 형식의 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bade-116">-DefaultProfile</span></span>
<span data-ttu-id="7bade-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="7bade-118">-PassName</span></span>
<span data-ttu-id="7bade-119">콘텐츠가 적용되는 통과의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="7bade-120">유일한 허용되는 값은 oobeSystem입니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7bade-121">-SettingName</span></span>
<span data-ttu-id="7bade-122">콘텐츠가 적용되는 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="7bade-123">이 매개 변수에 대해 허용되는 값은:</span><span class="sxs-lookup"><span data-stu-id="7bade-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="7bade-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="7bade-124">FirstLogonCommands</span></span>
- <span data-ttu-id="7bade-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="7bade-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7bade-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7bade-127">가상 머신 확장 **집합 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="7bade-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="7bade-128">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7bade-129">-Confirm</span></span>
<span data-ttu-id="7bade-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bade-131">-WhatIf</span></span>
<span data-ttu-id="7bade-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bade-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bade-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bade-134">CommonParameters</span></span>
<span data-ttu-id="7bade-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bade-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bade-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bade-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bade-137">입력</span><span class="sxs-lookup"><span data-stu-id="7bade-137">INPUTS</span></span>

### <span data-ttu-id="7bade-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7bade-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7bade-139">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7bade-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7bade-140">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7bade-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7bade-141">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7bade-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7bade-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7bade-142">System.String</span></span>

## <span data-ttu-id="7bade-143">출력</span><span class="sxs-lookup"><span data-stu-id="7bade-143">OUTPUTS</span></span>

### <span data-ttu-id="7bade-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7bade-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7bade-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7bade-145">NOTES</span></span>

## <span data-ttu-id="7bade-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bade-146">RELATED LINKS</span></span>

[<span data-ttu-id="7bade-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7bade-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
