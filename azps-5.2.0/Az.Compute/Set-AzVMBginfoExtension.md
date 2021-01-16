---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363742"
---
# <span data-ttu-id="0e3e2-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="0e3e2-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="0e3e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e3e2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3e2-103">BGInfo 확장을 가상 머신에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="0e3e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e3e2-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="0e3e2-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3e2-106">**Set-AzVMBGInfoExtension** cmdlet은 BGInfo 확장을 가상 머신에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="0e3e2-107">예제</span><span class="sxs-lookup"><span data-stu-id="0e3e2-107">EXAMPLES</span></span>

### <span data-ttu-id="0e3e2-108">예제 1: 가상 머신에 대한 BGInfo 확장 추가</span><span class="sxs-lookup"><span data-stu-id="0e3e2-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="0e3e2-109">이 명령은 ContosoVM이라는 가상 머신에 BGInfo 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="0e3e2-110">이 명령은 가상 머신의 리소스 그룹 및 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="0e3e2-111">이 명령은 확장의 이름 및 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="0e3e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e3e2-112">PARAMETERS</span></span>

### <span data-ttu-id="0e3e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3e2-113">-DefaultProfile</span></span>
<span data-ttu-id="0e3e2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3e2-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0e3e2-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0e3e2-116">이 cmdlet은 Azure 게스트 에이전트가 확장을 최신 부 버전으로 자동으로 업데이트하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="0e3e2-117">기본적으로 이 cmdlet을 사용하면 게스트 에이전트가 확장을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e2-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="0e3e2-118">-ForceRerun</span></span>
<span data-ttu-id="0e3e2-119">확장을 동일한 공용 또는 보호된 설정으로 다시 실행해야 한다고 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="0e3e2-120">값은 현재 값과 다른 문자열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="0e3e2-121">forceUpdateTag가 변경되지 않은 경우 공용 또는 보호된 설정에 대한 업데이트는 처리기에서 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e2-122">-Location</span><span class="sxs-lookup"><span data-stu-id="0e3e2-122">-Location</span></span>
<span data-ttu-id="0e3e2-123">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0e3e2-124">-Name</span></span>
<span data-ttu-id="0e3e2-125">이 cmdlet이 가상 머신에 추가하는 BGInfo 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e2-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0e3e2-126">-NoWait</span></span>
<span data-ttu-id="0e3e2-127">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0e3e2-128">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0e3e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="0e3e2-130">이 cmdlet에서 확장을 추가하는 가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="0e3e2-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0e3e2-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="0e3e2-132">이 cmdlet이 가상 머신에 추가하는 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e2-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e3e2-133">-VMName</span></span>
<span data-ttu-id="0e3e2-134">이 cmdlet에서 BGInfo 확장을 추가하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="0e3e2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e3e2-135">-Confirm</span></span>
<span data-ttu-id="0e3e2-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3e2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3e2-137">-WhatIf</span></span>
<span data-ttu-id="0e3e2-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0e3e2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3e2-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3e2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3e2-140">CommonParameters</span></span>
<span data-ttu-id="0e3e2-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3e2-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e3e2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3e2-143">입력</span><span class="sxs-lookup"><span data-stu-id="0e3e2-143">INPUTS</span></span>

### <span data-ttu-id="0e3e2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0e3e2-144">System.String</span></span>

### <span data-ttu-id="0e3e2-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0e3e2-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0e3e2-146">출력</span><span class="sxs-lookup"><span data-stu-id="0e3e2-146">OUTPUTS</span></span>

### <span data-ttu-id="0e3e2-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0e3e2-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0e3e2-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e3e2-148">NOTES</span></span>

## <span data-ttu-id="0e3e2-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e3e2-149">RELATED LINKS</span></span>
