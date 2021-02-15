---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177564"
---
# <span data-ttu-id="1bf7f-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1bf7f-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="1bf7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf7f-103">가상 머신에서 Chef 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="1bf7f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1bf7f-104">SYNTAX</span></span>

### <span data-ttu-id="1bf7f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="1bf7f-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf7f-106">Windows</span><span class="sxs-lookup"><span data-stu-id="1bf7f-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf7f-107">설명</span><span class="sxs-lookup"><span data-stu-id="1bf7f-107">DESCRIPTION</span></span>
<span data-ttu-id="1bf7f-108">**Remove-AzVMChefExtension** cmdlet은 가상 머신에서 Chef 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="1bf7f-109">예제</span><span class="sxs-lookup"><span data-stu-id="1bf7f-109">EXAMPLES</span></span>

### <span data-ttu-id="1bf7f-110">예제 1: Windows 가상 머신에서 Chef 확장 제거</span><span class="sxs-lookup"><span data-stu-id="1bf7f-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="1bf7f-111">이 명령은 ResourceGroup001이라는 리소스 그룹에 속하는 WindowsVM001이라는 Windows 기반 가상 머신에서 Chef 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="1bf7f-112">예제 2: Linux 가상 머신에서 Chef 확장 제거</span><span class="sxs-lookup"><span data-stu-id="1bf7f-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="1bf7f-113">이 명령은 ResourceGroup002 리소스 그룹에 속하는 Linux 기반 가상 머신 LinuxVM001에서 Chef 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="1bf7f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf7f-114">PARAMETERS</span></span>

### <span data-ttu-id="1bf7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf7f-115">-DefaultProfile</span></span>
<span data-ttu-id="1bf7f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf7f-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="1bf7f-117">-Linux</span></span>
<span data-ttu-id="1bf7f-118">이 cmdlet이 Linux 가상 머신을 대상으로 하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf7f-119">-Name</span></span>
<span data-ttu-id="1bf7f-120">이 cmdlet이 제거하는 Chef 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1bf7f-121">-NoWait</span></span>
<span data-ttu-id="1bf7f-122">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1bf7f-123">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf7f-124">-ResourceGroupName</span></span>
<span data-ttu-id="1bf7f-125">가상 머신을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="1bf7f-126">-VMName</span></span>
<span data-ttu-id="1bf7f-127">이 cmdlet이 Chef 확장을 제거하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="1bf7f-128">-Windows</span></span>
<span data-ttu-id="1bf7f-129">이 cmdlet이 Windows 가상 머신을 대상으로 하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bf7f-130">-Confirm</span></span>
<span data-ttu-id="1bf7f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf7f-132">-WhatIf</span></span>
<span data-ttu-id="1bf7f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1bf7f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf7f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf7f-135">CommonParameters</span></span>
<span data-ttu-id="1bf7f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf7f-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1bf7f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf7f-138">입력</span><span class="sxs-lookup"><span data-stu-id="1bf7f-138">INPUTS</span></span>

### <span data-ttu-id="1bf7f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf7f-139">System.String</span></span>

## <span data-ttu-id="1bf7f-140">출력</span><span class="sxs-lookup"><span data-stu-id="1bf7f-140">OUTPUTS</span></span>

### <span data-ttu-id="1bf7f-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1bf7f-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1bf7f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1bf7f-142">NOTES</span></span>

## <span data-ttu-id="1bf7f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bf7f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1bf7f-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1bf7f-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="1bf7f-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1bf7f-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
