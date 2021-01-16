---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352041"
---
# <span data-ttu-id="36c47-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="36c47-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="36c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36c47-102">SYNOPSIS</span></span>
<span data-ttu-id="36c47-103">무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="36c47-104">구문</span><span class="sxs-lookup"><span data-stu-id="36c47-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36c47-105">설명</span><span class="sxs-lookup"><span data-stu-id="36c47-105">DESCRIPTION</span></span>
<span data-ttu-id="36c47-106">**Add-AzVmssAdditionalUnattendContent** cmdlet은 무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="36c47-107">예제</span><span class="sxs-lookup"><span data-stu-id="36c47-107">EXAMPLES</span></span>

### <span data-ttu-id="36c47-108">예제 1: 무인 Windows 설정 답변 파일에 정보 추가</span><span class="sxs-lookup"><span data-stu-id="36c47-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="36c47-109">이 명령은 무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="36c47-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36c47-110">PARAMETERS</span></span>

### <span data-ttu-id="36c47-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="36c47-111">-ComponentName</span></span>
<span data-ttu-id="36c47-112">추가된 콘텐츠로 구성할 구성 요소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="36c47-113">허용되는 유일한 값은 Microsoft-Windows-Shell-Setup입니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="36c47-114">-Content</span><span class="sxs-lookup"><span data-stu-id="36c47-114">-Content</span></span>
<span data-ttu-id="36c47-115">지정된 경로 및 구성 요소에 대해 unattend.xml XML 형식의 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="36c47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c47-116">-DefaultProfile</span></span>
<span data-ttu-id="36c47-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36c47-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="36c47-118">-PassName</span></span>
<span data-ttu-id="36c47-119">콘텐츠가 적용되는 통과의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="36c47-120">유일하게 허용되는 값은 oobeSystem입니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="36c47-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="36c47-121">-SettingName</span></span>
<span data-ttu-id="36c47-122">콘텐츠가 적용되는 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="36c47-123">이 매개 변수에 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="36c47-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="36c47-124">FirstLogonCommands</span></span>
- <span data-ttu-id="36c47-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="36c47-125">AutoLogon</span></span>

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

### <span data-ttu-id="36c47-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36c47-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="36c47-127">가상 머신 **확장 집합 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="36c47-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="36c47-128">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="36c47-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36c47-129">-Confirm</span></span>
<span data-ttu-id="36c47-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36c47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c47-131">-WhatIf</span></span>
<span data-ttu-id="36c47-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="36c47-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36c47-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36c47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c47-134">CommonParameters</span></span>
<span data-ttu-id="36c47-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36c47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c47-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36c47-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c47-137">입력</span><span class="sxs-lookup"><span data-stu-id="36c47-137">INPUTS</span></span>

### <span data-ttu-id="36c47-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36c47-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="36c47-139">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="36c47-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="36c47-140">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="36c47-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="36c47-141">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="36c47-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="36c47-142">System.String</span><span class="sxs-lookup"><span data-stu-id="36c47-142">System.String</span></span>

## <span data-ttu-id="36c47-143">출력</span><span class="sxs-lookup"><span data-stu-id="36c47-143">OUTPUTS</span></span>

### <span data-ttu-id="36c47-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36c47-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="36c47-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36c47-145">NOTES</span></span>

## <span data-ttu-id="36c47-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36c47-146">RELATED LINKS</span></span>

[<span data-ttu-id="36c47-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="36c47-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
