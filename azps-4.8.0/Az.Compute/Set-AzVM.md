---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213088"
---
# <span data-ttu-id="c0d2b-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0d2b-101">Set-AzVM</span></span>

## <span data-ttu-id="c0d2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d2b-103">가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="c0d2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0d2b-104">SYNTAX</span></span>

### <span data-ttu-id="c0d2b-105">GeneralizeResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0d2b-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d2b-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0d2b-113">설명은</span><span class="sxs-lookup"><span data-stu-id="c0d2b-113">DESCRIPTION</span></span>
<span data-ttu-id="c0d2b-114">**AzVM** cmdlet은 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="c0d2b-115">이 cmdlet을 실행 하기 전에 가상 컴퓨터에 로그온 하 고 Sysprep를 사용 하 여 하드 디스크를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="c0d2b-116">예제의</span><span class="sxs-lookup"><span data-stu-id="c0d2b-116">EXAMPLES</span></span>

### <span data-ttu-id="c0d2b-117">예제 1: 가상 컴퓨터를 일반화로 표시</span><span class="sxs-lookup"><span data-stu-id="c0d2b-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="c0d2b-118">이 명령은 VirtualMachine07 이라는 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="c0d2b-119">변수</span><span class="sxs-lookup"><span data-stu-id="c0d2b-119">PARAMETERS</span></span>

### <span data-ttu-id="c0d2b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0d2b-120">-AsJob</span></span>
<span data-ttu-id="c0d2b-121">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c0d2b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d2b-122">-DefaultProfile</span></span>
<span data-ttu-id="c0d2b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0d2b-124">일반화</span><span class="sxs-lookup"><span data-stu-id="c0d2b-124">-Generalized</span></span>
<span data-ttu-id="c0d2b-125">이 cmdlet이 가상 컴퓨터를 일반화 된 것으로 표시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="c0d2b-126">-Id</span><span class="sxs-lookup"><span data-stu-id="c0d2b-126">-Id</span></span>
<span data-ttu-id="c0d2b-127">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c0d2b-128">-이름</span><span class="sxs-lookup"><span data-stu-id="c0d2b-128">-Name</span></span>
<span data-ttu-id="c0d2b-129">이 cmdlet이 작동 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0d2b-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0d2b-130">-NoWait</span></span>
<span data-ttu-id="c0d2b-131">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c0d2b-132">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c0d2b-133">-재적용</span><span class="sxs-lookup"><span data-stu-id="c0d2b-133">-Reapply</span></span>
<span data-ttu-id="c0d2b-134">가상 컴퓨터를 다시 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="c0d2b-135">-재배포</span><span class="sxs-lookup"><span data-stu-id="c0d2b-135">-Redeploy</span></span>
<span data-ttu-id="c0d2b-136">이 cmdlet이 가상 컴퓨터를 다른 Azure 호스트에 수동으로 다시 배포 하 여 문제를 해결 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="c0d2b-137">가상 컴퓨터를 다시 배포 하는 경우 삭제 되 고,이로 인해 임시 드라이브 데이터가 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="c0d2b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d2b-138">-ResourceGroupName</span></span>
<span data-ttu-id="c0d2b-139">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c0d2b-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="c0d2b-140">-SimulateEviction</span></span>
<span data-ttu-id="c0d2b-141">이 cmdlet이 스폿 가상 컴퓨터의 제거를 시뮬레이션 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="c0d2b-142">제거는 API를 호출 하는 30 분 내에 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="c0d2b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d2b-143">CommonParameters</span></span>
<span data-ttu-id="c0d2b-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d2b-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d2b-146">입력</span><span class="sxs-lookup"><span data-stu-id="c0d2b-146">INPUTS</span></span>

### <span data-ttu-id="c0d2b-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0d2b-147">System.String</span></span>

## <span data-ttu-id="c0d2b-148">출력</span><span class="sxs-lookup"><span data-stu-id="c0d2b-148">OUTPUTS</span></span>

### <span data-ttu-id="c0d2b-149">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="c0d2b-150">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c0d2b-151">상속자</span><span class="sxs-lookup"><span data-stu-id="c0d2b-151">NOTES</span></span>

## <span data-ttu-id="c0d2b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0d2b-152">RELATED LINKS</span></span>

[<span data-ttu-id="c0d2b-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0d2b-153">Get-AzVM</span></span>](./Get-AzVM.md)


