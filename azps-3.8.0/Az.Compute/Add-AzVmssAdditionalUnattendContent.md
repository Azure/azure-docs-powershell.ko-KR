---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043442"
---
# <span data-ttu-id="d10c6-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="d10c6-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="d10c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d10c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d10c6-103">무인 Windows 설치 응답 파일에 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d10c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d10c6-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d10c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d10c6-106">**추가-AzVmssAdditionalUnattendContent** cmdlet은 정보를 무인 Windows 설치 응답 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d10c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d10c6-107">EXAMPLES</span></span>

### <span data-ttu-id="d10c6-108">예제 1: 무인 Windows 설치 응답 파일에 정보 추가</span><span class="sxs-lookup"><span data-stu-id="d10c6-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="d10c6-109">이 명령은 무인 Windows 설치 응답 파일에 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d10c6-110">변수</span><span class="sxs-lookup"><span data-stu-id="d10c6-110">PARAMETERS</span></span>

### <span data-ttu-id="d10c6-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d10c6-111">-ComponentName</span></span>
<span data-ttu-id="d10c6-112">추가 된 콘텐츠를 사용 하 여 구성할 구성 요소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="d10c6-113">유일 하 게 허용 되는 값은 Microsoft-Windows-셸 설치입니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="d10c6-114">-콘텐츠</span><span class="sxs-lookup"><span data-stu-id="d10c6-114">-Content</span></span>
<span data-ttu-id="d10c6-115">지정 된 경로와 구성 요소의 unattend.xml 파일에 추가 되는 XML 서식 지정 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="d10c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10c6-116">-DefaultProfile</span></span>
<span data-ttu-id="d10c6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d10c6-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="d10c6-118">-PassName</span></span>
<span data-ttu-id="d10c6-119">콘텐츠가 적용 되는 패스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="d10c6-120">유일 하 게 허용 되는 값은 oobeSystem입니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="d10c6-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d10c6-121">-SettingName</span></span>
<span data-ttu-id="d10c6-122">콘텐츠가 적용 되는 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="d10c6-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="d10c6-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="d10c6-124">FirstLogonCommands</span></span>
- <span data-ttu-id="d10c6-125">자동</span><span class="sxs-lookup"><span data-stu-id="d10c6-125">AutoLogon</span></span>

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

### <span data-ttu-id="d10c6-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d10c6-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d10c6-127">가상 컴퓨터 **크기 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="d10c6-128">[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d10c6-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d10c6-129">-Confirm</span></span>
<span data-ttu-id="d10c6-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10c6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10c6-131">-WhatIf</span></span>
<span data-ttu-id="d10c6-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d10c6-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10c6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10c6-134">CommonParameters</span></span>
<span data-ttu-id="d10c6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d10c6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10c6-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d10c6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10c6-137">입력</span><span class="sxs-lookup"><span data-stu-id="d10c6-137">INPUTS</span></span>

### <span data-ttu-id="d10c6-138">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="d10c6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d10c6-139">시스템 Null 허용 ' 1 [[PassNames, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d10c6-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d10c6-140">시스템 Null 허용 ' 1 [[23.0.0.0 이름, Microsoft azure. Management. 관리. t e t/. i =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d10c6-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d10c6-141">시스템 Null 허용 ' 1 [[23.0.0.0]. SettingNames, Microsoft Azure. 관리. t e t =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d10c6-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d10c6-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d10c6-142">System.String</span></span>

## <span data-ttu-id="d10c6-143">출력</span><span class="sxs-lookup"><span data-stu-id="d10c6-143">OUTPUTS</span></span>

### <span data-ttu-id="d10c6-144">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="d10c6-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d10c6-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d10c6-145">NOTES</span></span>

## <span data-ttu-id="d10c6-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d10c6-146">RELATED LINKS</span></span>

[<span data-ttu-id="d10c6-147">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d10c6-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
