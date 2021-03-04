---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: daf1a9c738e6e4d0d97a22eedc8355750d15ec72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004528"
---
# <span data-ttu-id="e0beb-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-101">Start-AzVM</span></span>

## <span data-ttu-id="e0beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0beb-102">SYNOPSIS</span></span>
<span data-ttu-id="e0beb-103">Azure 가상 머신을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e0beb-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0beb-104">SYNTAX</span></span>

### <span data-ttu-id="e0beb-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e0beb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0beb-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e0beb-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0beb-107">설명</span><span class="sxs-lookup"><span data-stu-id="e0beb-107">DESCRIPTION</span></span>
<span data-ttu-id="e0beb-108">**Start-AzVM** cmdlet은 Azure 가상 머신을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e0beb-109">예제</span><span class="sxs-lookup"><span data-stu-id="e0beb-109">EXAMPLES</span></span>

### <span data-ttu-id="e0beb-110">예제 1: 가상 머신 시작</span><span class="sxs-lookup"><span data-stu-id="e0beb-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e0beb-111">이 명령은 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e0beb-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0beb-112">PARAMETERS</span></span>

### <span data-ttu-id="e0beb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0beb-113">-AsJob</span></span>
<span data-ttu-id="e0beb-114">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e0beb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0beb-115">-DefaultProfile</span></span>
<span data-ttu-id="e0beb-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0beb-117">-Id</span><span class="sxs-lookup"><span data-stu-id="e0beb-117">-Id</span></span>
<span data-ttu-id="e0beb-118">가상 머신의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0beb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e0beb-119">-Name</span></span>
<span data-ttu-id="e0beb-120">가상 머신 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0beb-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0beb-121">-NoWait</span></span>
<span data-ttu-id="e0beb-122">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e0beb-123">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e0beb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0beb-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0beb-125">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0beb-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e0beb-126">-Confirm</span></span>
<span data-ttu-id="e0beb-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0beb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0beb-128">-WhatIf</span></span>
<span data-ttu-id="e0beb-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0beb-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0beb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0beb-131">CommonParameters</span></span>
<span data-ttu-id="e0beb-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0beb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0beb-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0beb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0beb-134">입력</span><span class="sxs-lookup"><span data-stu-id="e0beb-134">INPUTS</span></span>

### <span data-ttu-id="e0beb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e0beb-135">System.String</span></span>

## <span data-ttu-id="e0beb-136">출력</span><span class="sxs-lookup"><span data-stu-id="e0beb-136">OUTPUTS</span></span>

### <span data-ttu-id="e0beb-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e0beb-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="e0beb-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e0beb-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e0beb-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0beb-139">NOTES</span></span>

## <span data-ttu-id="e0beb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0beb-140">RELATED LINKS</span></span>

[<span data-ttu-id="e0beb-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e0beb-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e0beb-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e0beb-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e0beb-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e0beb-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e0beb-146">Update-AzVM</span></span>](./Update-AzVM.md)


