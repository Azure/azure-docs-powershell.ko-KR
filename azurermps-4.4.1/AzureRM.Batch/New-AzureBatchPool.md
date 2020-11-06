---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531188"
---
# <span data-ttu-id="57e8a-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="57e8a-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="57e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="57e8a-103">일괄 처리 서비스에서 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57e8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57e8a-104">SYNTAX</span></span>

### <span data-ttu-id="57e8a-105">CloudServiceAndTargetDedicated (기본값)</span><span class="sxs-lookup"><span data-stu-id="57e8a-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57e8a-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="57e8a-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57e8a-107">CloudServiceAndAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="57e8a-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57e8a-108">VirtualMachineAndAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="57e8a-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57e8a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="57e8a-109">DESCRIPTION</span></span>
<span data-ttu-id="57e8a-110">**새-AzureBatchPool** Cmdlet은 *batchcontext* 매개 변수에서 지정 하는 계정 아래에서 Azure 일괄 처리 서비스에 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="57e8a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="57e8a-111">EXAMPLES</span></span>

### <span data-ttu-id="57e8a-112">예제 1: TargetDedicated 매개 변수 집합을 사용 하 여 새 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="57e8a-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="57e8a-113">이 명령은 TargetDedicated 매개 변수 집합을 사용 하 여 ID MyPool 인 새 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="57e8a-114">대상 할당은 3 개의 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="57e8a-115">풀은 제품군 4의 최신 운영 체제 버전으로 이미지 된 작은 가상 컴퓨터를 사용 하도록 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="57e8a-116">예제 2: 자동 크기 조정 매개 변수 집합을 사용 하 여 새 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="57e8a-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="57e8a-117">이 명령은 자동 크기 조정 매개 변수 집합을 사용 하 여 ID AutoScalePool 인 새 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="57e8a-118">풀은 최신 운영 체제 버전의 패밀리 4를 사용 하 여 이미지를 지정 하 고, 대상 계산 노드의 수는 자동 크기 조정 수식에 의해 결정 됨을 기준으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="57e8a-119">변수</span><span class="sxs-lookup"><span data-stu-id="57e8a-119">PARAMETERS</span></span>

### <span data-ttu-id="57e8a-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="57e8a-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="57e8a-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="57e8a-122">크기 자동 조정 수식에 따라 풀 크기가 자동으로 조정 되기 전 까지의 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="57e8a-123">기본값은 15 분 이며 최소 값은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="57e8a-124">-AutoScaleFormula</span></span>
<span data-ttu-id="57e8a-125">자동으로 수영장의 크기를 조정 하는 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="57e8a-126">-BatchContext</span></span>
<span data-ttu-id="57e8a-127">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="57e8a-128">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="57e8a-129">-CertificateReferences</span></span>
<span data-ttu-id="57e8a-130">풀과 연결 된 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="57e8a-131">일괄 처리 서비스는 풀의 각 계산 노드에 참조 된 인증서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e8a-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="57e8a-133">Azure 클라우드 서비스 플랫폼에 따라 풀에 대 한 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57e8a-134">-DisplayName</span></span>
<span data-ttu-id="57e8a-135">풀의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-135">Specifies the display name of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-136">-Id</span><span class="sxs-lookup"><span data-stu-id="57e8a-136">-Id</span></span>
<span data-ttu-id="57e8a-137">만들 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="57e8a-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="57e8a-139">이 cmdlet이 전용 계산 노드 간의 직접적인 통신을 위해 풀을 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="57e8a-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="57e8a-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="57e8a-141">단일 계산 노드에서 실행할 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="57e8a-142">-Metadata</span></span>
<span data-ttu-id="57e8a-143">새 풀에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="57e8a-144">키는 메타 데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-144">The key is the metadata name.</span></span>
<span data-ttu-id="57e8a-145">값은 메타 데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e8a-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="57e8a-147">-ResizeTimeout</span></span>
<span data-ttu-id="57e8a-148">풀에 계산 노드를 할당 하는 시간 초과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="57e8a-149">-StartTask</span></span>
<span data-ttu-id="57e8a-150">풀에 대 한 작업 시작 사양을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="57e8a-151">계산 노드가 풀을 조인 하거나 계산 노드가 다시 부팅 되거나 reimaged 경우 시작 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="57e8a-152">-TargetDedicated</span></span>
<span data-ttu-id="57e8a-153">풀에 할당할 계산 노드의 대상 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="57e8a-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="57e8a-155">ComputeNodeFillType 같은 작업 일정 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e8a-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="57e8a-157">가상 컴퓨터 인프라의 풀에 대 한 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="57e8a-158">-VirtualMachineSize</span></span>
<span data-ttu-id="57e8a-159">풀의 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="57e8a-160">가상 컴퓨터 크기에 대 한 자세한 내용은 https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure 사이트의 가상 컴퓨터 크기를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57e8a-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-161">-확인</span><span class="sxs-lookup"><span data-stu-id="57e8a-161">-Confirm</span></span>
<span data-ttu-id="57e8a-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e8a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e8a-163">-WhatIf</span></span>
<span data-ttu-id="57e8a-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57e8a-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e8a-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e8a-166">-DefaultProfile</span></span>
<span data-ttu-id="57e8a-167">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e8a-168">CommonParameters</span></span>
<span data-ttu-id="57e8a-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e8a-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e8a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e8a-171">입력</span><span class="sxs-lookup"><span data-stu-id="57e8a-171">INPUTS</span></span>

### <span data-ttu-id="57e8a-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="57e8a-172">BatchAccountContext</span></span>
<span data-ttu-id="57e8a-173">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="57e8a-174">출력</span><span class="sxs-lookup"><span data-stu-id="57e8a-174">OUTPUTS</span></span>

## <span data-ttu-id="57e8a-175">상속자</span><span class="sxs-lookup"><span data-stu-id="57e8a-175">NOTES</span></span>

## <span data-ttu-id="57e8a-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57e8a-176">RELATED LINKS</span></span>

[<span data-ttu-id="57e8a-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="57e8a-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="57e8a-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="57e8a-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="57e8a-179">-AzureBatchPool 제거</span><span class="sxs-lookup"><span data-stu-id="57e8a-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="57e8a-180">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57e8a-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


