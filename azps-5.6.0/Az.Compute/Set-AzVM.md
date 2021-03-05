---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b42f456b45de0e78b9d9e0c371dca950ada88ded
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977499"
---
# <span data-ttu-id="42ae3-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="42ae3-101">Set-AzVM</span></span>

## <span data-ttu-id="42ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="42ae3-103">가상 머신을 일반화된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="42ae3-104">구문</span><span class="sxs-lookup"><span data-stu-id="42ae3-104">SYNTAX</span></span>

### <span data-ttu-id="42ae3-105">GeneralizeResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="42ae3-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ae3-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ae3-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ae3-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ae3-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ae3-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42ae3-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42ae3-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="42ae3-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42ae3-113">설명</span><span class="sxs-lookup"><span data-stu-id="42ae3-113">DESCRIPTION</span></span>
<span data-ttu-id="42ae3-114">**Set-AzVM** cmdlet은 가상 머신을 일반화된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="42ae3-115">이 cmdlet을 실행하기 전에 가상 머신에 로그온하고 Sysprep를 사용하여 하드 디스크를 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="42ae3-116">예제</span><span class="sxs-lookup"><span data-stu-id="42ae3-116">EXAMPLES</span></span>

### <span data-ttu-id="42ae3-117">예제 1: 가상 머신을 일반화된 것으로 표시</span><span class="sxs-lookup"><span data-stu-id="42ae3-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="42ae3-118">이 명령은 VirtualMachine07이라는 가상 머신을 일반화된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="42ae3-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42ae3-119">PARAMETERS</span></span>

### <span data-ttu-id="42ae3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42ae3-120">-AsJob</span></span>
<span data-ttu-id="42ae3-121">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="42ae3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ae3-122">-DefaultProfile</span></span>
<span data-ttu-id="42ae3-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42ae3-124">-일반화</span><span class="sxs-lookup"><span data-stu-id="42ae3-124">-Generalized</span></span>
<span data-ttu-id="42ae3-125">이 cmdlet은 가상 머신을 일반화된 것으로 표시하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-126">-Id</span><span class="sxs-lookup"><span data-stu-id="42ae3-126">-Id</span></span>
<span data-ttu-id="42ae3-127">가상 머신의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="42ae3-128">-Name</span></span>
<span data-ttu-id="42ae3-129">이 cmdlet이 작동하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="42ae3-130">-NoWait</span></span>
<span data-ttu-id="42ae3-131">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="42ae3-132">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-133">-다시신고</span><span class="sxs-lookup"><span data-stu-id="42ae3-133">-Reapply</span></span>
<span data-ttu-id="42ae3-134">가상 머신을 다시 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="42ae3-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-135">-재배포</span><span class="sxs-lookup"><span data-stu-id="42ae3-135">-Redeploy</span></span>
<span data-ttu-id="42ae3-136">이 cmdlet은 가상 머신을 다른 Azure 호스트로 수동으로 다시 재배포하여 문제를 해결했다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="42ae3-137">가상 머신을 다시 재배포하면 가상 머신이 다시 시작됩니다. 이로 인하여 에메랄드 드라이브 데이터가 손실됩니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ae3-138">-ResourceGroupName</span></span>
<span data-ttu-id="42ae3-139">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="42ae3-140">-SimulateEviction</span></span>
<span data-ttu-id="42ae3-141">이 cmdlet은 스폿 가상 머신의 터전을 시뮬레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="42ae3-142">API를 호출한 후 30분 이내에 은닉이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ae3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ae3-143">CommonParameters</span></span>
<span data-ttu-id="42ae3-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42ae3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ae3-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42ae3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ae3-146">입력</span><span class="sxs-lookup"><span data-stu-id="42ae3-146">INPUTS</span></span>

### <span data-ttu-id="42ae3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="42ae3-147">System.String</span></span>

## <span data-ttu-id="42ae3-148">출력</span><span class="sxs-lookup"><span data-stu-id="42ae3-148">OUTPUTS</span></span>

### <span data-ttu-id="42ae3-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="42ae3-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="42ae3-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="42ae3-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="42ae3-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42ae3-151">NOTES</span></span>

## <span data-ttu-id="42ae3-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42ae3-152">RELATED LINKS</span></span>

[<span data-ttu-id="42ae3-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="42ae3-153">Get-AzVM</span></span>](./Get-AzVM.md)


