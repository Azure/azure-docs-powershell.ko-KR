---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 403bcc5a85001b6d98c67f91d995eb05bc948752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182057"
---
# <span data-ttu-id="619c1-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="619c1-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="619c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="619c1-102">SYNOPSIS</span></span>
<span data-ttu-id="619c1-103">Azure Storage 컨테이너에 계산 노드 서비스 로그 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="619c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="619c1-104">SYNTAX</span></span>

### <span data-ttu-id="619c1-105">AzureBatchComputeNodeServiceLogUpload(기본값)</span><span class="sxs-lookup"><span data-stu-id="619c1-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="619c1-106">ID</span><span class="sxs-lookup"><span data-stu-id="619c1-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619c1-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="619c1-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="619c1-108">설명</span><span class="sxs-lookup"><span data-stu-id="619c1-108">DESCRIPTION</span></span>
<span data-ttu-id="619c1-109">이 cmdlet은 오류가 발생하고 Azure 지원으로 에스컬레이터하려면 계산 노드에서 Azure Batch 서비스 로그 파일을 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="619c1-110">Azure Batch 서비스 로그 파일은 Batch 서비스로 문제를 디버깅하는 데 도움을 주기 위해 Azure 지원과 공유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="619c1-111">예제</span><span class="sxs-lookup"><span data-stu-id="619c1-111">EXAMPLES</span></span>

### <span data-ttu-id="619c1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="619c1-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="619c1-113">2018년 1월 1일 자정 또는 이후에 작성된 계산 노드 서비스 로그를 업로드합니다. 이 로그는 계산 노드에서 얻은 것으로, 계산 노드가 상주하는 풀의 풀 ID 및 계산 노드 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="619c1-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="619c1-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="619c1-115">계산 노드에서 얻은 2018년 1월 1일 자정 및 2018년 1월 10일 자정 이후에 기록된 계산 노드 서비스 로그, 계산 노드가 상주하는 풀의 풀 ID 및 계산 노드 ID를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="619c1-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="619c1-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="619c1-117">계산 노드 개체에서 얻은 2018년 1월 1일 자정 및 2018년 1월 10일 자정 이전으로 기록된 계산 노드 서비스 로그를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="619c1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="619c1-118">PARAMETERS</span></span>

### <span data-ttu-id="619c1-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="619c1-119">-BatchContext</span></span>
<span data-ttu-id="619c1-120">Batch 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="619c1-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="619c1-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="619c1-123">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="619c1-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="619c1-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="619c1-125">-ComputeNode</span></span>
<span data-ttu-id="619c1-126">서비스 로그가 검색되는 **PSComputeNode** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="619c1-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="619c1-127">-ComputeNodeId</span></span>
<span data-ttu-id="619c1-128">계산 노드의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="619c1-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="619c1-129">-ContainerUrl</span></span>
<span data-ttu-id="619c1-130">Azure Storage에 대한 컨테이너 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="619c1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619c1-131">-DefaultProfile</span></span>
<span data-ttu-id="619c1-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="619c1-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="619c1-133">-EndTime</span></span>
<span data-ttu-id="619c1-134">업로드할 서비스 로그의 종료 시간(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="619c1-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="619c1-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="619c1-135">-PoolId</span></span>
<span data-ttu-id="619c1-136">계산 노드를 포함하는 풀의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="619c1-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="619c1-137">-StartTime</span></span>
<span data-ttu-id="619c1-138">업로드할 서비스 로그의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="619c1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="619c1-139">-Confirm</span></span>
<span data-ttu-id="619c1-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="619c1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="619c1-141">-WhatIf</span></span>
<span data-ttu-id="619c1-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="619c1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="619c1-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="619c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619c1-144">CommonParameters</span></span>
<span data-ttu-id="619c1-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="619c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619c1-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="619c1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619c1-147">입력</span><span class="sxs-lookup"><span data-stu-id="619c1-147">INPUTS</span></span>

### <span data-ttu-id="619c1-148">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="619c1-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="619c1-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="619c1-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="619c1-150">출력</span><span class="sxs-lookup"><span data-stu-id="619c1-150">OUTPUTS</span></span>

### <span data-ttu-id="619c1-151">Microsoft.Azure.Commands.Batch. Models.PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="619c1-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="619c1-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="619c1-152">NOTES</span></span>

## <span data-ttu-id="619c1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="619c1-153">RELATED LINKS</span></span>
