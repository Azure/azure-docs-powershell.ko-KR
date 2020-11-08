---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 403bcc5a85001b6d98c67f91d995eb05bc948752
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204083"
---
# <span data-ttu-id="4f834-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="4f834-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="4f834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f834-102">SYNOPSIS</span></span>
<span data-ttu-id="4f834-103">Azure 저장소 컨테이너에 계산 노드 서비스 로그 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="4f834-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f834-104">SYNTAX</span></span>

### <span data-ttu-id="4f834-105">AzureBatchComputeNodeServiceLogUpload (기본값)</span><span class="sxs-lookup"><span data-stu-id="4f834-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f834-106">I</span><span class="sxs-lookup"><span data-stu-id="4f834-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f834-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="4f834-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f834-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4f834-108">DESCRIPTION</span></span>
<span data-ttu-id="4f834-109">오류가 발생 하 여 Azure 지원으로 에스컬레이션 하려는 경우이 cmdlet은 계산 노드에서 Azure Batch service 로그 파일을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="4f834-110">일괄 서비스의 디버깅 문제를 지원 하려면 Azure Batch service 로그 파일을 Azure 지원으로 공유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="4f834-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4f834-111">EXAMPLES</span></span>

### <span data-ttu-id="4f834-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f834-112">Example 1</span></span>
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

<span data-ttu-id="4f834-113">계산 노드, 계산 노드가 상주 하는 풀의 지정 된 풀 id, 계산 노드 id를 기준으로 생성 된 2018 년 1 월 1 일 또는 그 이후 기록 되는 계산 노드 서비스 로그를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="4f834-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="4f834-114">Example 2</span></span>
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

<span data-ttu-id="4f834-115">계산 노드, 계산 노드가 상주 하는 풀의 지정 된 풀 id, 계산 노드 id 등의 2018 10 월 2018 1 일 또는 그 이전에 작성 된 계산 노드 서비스 로그를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="4f834-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="4f834-116">Example 3</span></span>
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

<span data-ttu-id="4f834-117">계산 노드 개체에서 얻은 자정 1 월 2018 10 일 자정 이전 2018에 작성 된 계산 노드 서비스 로그를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="4f834-118">변수</span><span class="sxs-lookup"><span data-stu-id="4f834-118">PARAMETERS</span></span>

### <span data-ttu-id="4f834-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4f834-119">-BatchContext</span></span>
<span data-ttu-id="4f834-120">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="4f834-121">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="4f834-122">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="4f834-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="4f834-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4f834-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="4f834-125">-ComputeNode</span></span>
<span data-ttu-id="4f834-126">서비스 로그가 검색 되는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="4f834-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="4f834-127">-ComputeNodeId</span></span>
<span data-ttu-id="4f834-128">계산 노드의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="4f834-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="4f834-129">-ContainerUrl</span></span>
<span data-ttu-id="4f834-130">Azure Storage에 대 한 컨테이너 url입니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="4f834-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f834-131">-DefaultProfile</span></span>
<span data-ttu-id="4f834-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f834-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4f834-133">-EndTime</span></span>
<span data-ttu-id="4f834-134">업로드할 서비스 로그의 종료 시간입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="4f834-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="4f834-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4f834-135">-PoolId</span></span>
<span data-ttu-id="4f834-136">계산 노드를 포함 하는 풀의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="4f834-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4f834-137">-StartTime</span></span>
<span data-ttu-id="4f834-138">업로드할 서비스 로그의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="4f834-139">-확인</span><span class="sxs-lookup"><span data-stu-id="4f834-139">-Confirm</span></span>
<span data-ttu-id="4f834-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f834-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f834-141">-WhatIf</span></span>
<span data-ttu-id="4f834-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f834-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f834-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f834-144">CommonParameters</span></span>
<span data-ttu-id="4f834-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f834-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f834-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f834-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f834-147">입력</span><span class="sxs-lookup"><span data-stu-id="4f834-147">INPUTS</span></span>

### <span data-ttu-id="4f834-148">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4f834-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="4f834-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4f834-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4f834-150">출력</span><span class="sxs-lookup"><span data-stu-id="4f834-150">OUTPUTS</span></span>

### <span data-ttu-id="4f834-151">Microsoft.Azure.Commands.Batch. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="4f834-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="4f834-152">상속자</span><span class="sxs-lookup"><span data-stu-id="4f834-152">NOTES</span></span>

## <span data-ttu-id="4f834-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f834-153">RELATED LINKS</span></span>
