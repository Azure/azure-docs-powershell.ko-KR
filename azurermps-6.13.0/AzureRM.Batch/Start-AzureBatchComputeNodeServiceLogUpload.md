---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/Start-AzureBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8f171b42e3f1e1f087890ec451d5a3ff13cb8c57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531442"
---
# <span data-ttu-id="c3cac-101">Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c3cac-101">Start-AzureBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="c3cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3cac-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cac-103">Azure 저장소 컨테이너에 계산 노드 서비스 로그 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-103">Upload compute node service log files to an Azure Storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3cac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3cac-104">SYNTAX</span></span>

### <span data-ttu-id="c3cac-105">AzureBatchComputeNodeServiceLogUpload (기본값)</span><span class="sxs-lookup"><span data-stu-id="c3cac-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime>
 [-EndTime <DateTime>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cac-106">I</span><span class="sxs-lookup"><span data-stu-id="c3cac-106">Id</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String>
 [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cac-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="c3cac-107">ParentObject</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3cac-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c3cac-108">DESCRIPTION</span></span>
<span data-ttu-id="c3cac-109">오류가 발생 하 여 Azure 지원으로 에스컬레이션 하려는 경우이 cmdlet은 계산 노드에서 Azure Batch service 로그 파일을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="c3cac-110">일괄 서비스의 디버깅 문제를 지원 하려면 Azure Batch service 로그 파일을 Azure 지원으로 공유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="c3cac-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c3cac-111">EXAMPLES</span></span>

### <span data-ttu-id="c3cac-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3cac-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="c3cac-113">계산 노드, 계산 노드가 상주 하는 풀의 지정 된 풀 id, 계산 노드 id를 기준으로 생성 된 2018 년 1 월 1 일 또는 그 이후 기록 되는 계산 노드 서비스 로그를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="c3cac-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3cac-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="c3cac-115">계산 노드, 계산 노드가 상주 하는 풀의 지정 된 풀 id, 계산 노드 id 등의 2018 10 월 2018 1 일 또는 그 이전에 작성 된 계산 노드 서비스 로그를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="c3cac-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="c3cac-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="c3cac-117">계산 노드 개체에서 얻은 자정 1 월 2018 10 일 자정 이전 2018에 작성 된 계산 노드 서비스 로그를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="c3cac-118">변수</span><span class="sxs-lookup"><span data-stu-id="c3cac-118">PARAMETERS</span></span>

### <span data-ttu-id="c3cac-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3cac-119">-BatchContext</span></span>
<span data-ttu-id="c3cac-120">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="c3cac-121">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="c3cac-122">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="c3cac-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="c3cac-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3cac-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3cac-125">-ComputeNode</span></span>
<span data-ttu-id="c3cac-126">서비스 로그가 검색 되는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="c3cac-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c3cac-127">-ComputeNodeId</span></span>
<span data-ttu-id="c3cac-128">계산 노드의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="c3cac-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="c3cac-129">-ContainerUrl</span></span>
<span data-ttu-id="c3cac-130">Azure Storage에 대 한 컨테이너 url입니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="c3cac-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cac-131">-DefaultProfile</span></span>
<span data-ttu-id="c3cac-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3cac-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c3cac-133">-EndTime</span></span>
<span data-ttu-id="c3cac-134">업로드할 서비스 로그의 종료 시간입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="c3cac-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="c3cac-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c3cac-135">-PoolId</span></span>
<span data-ttu-id="c3cac-136">계산 노드를 포함 하는 풀의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="c3cac-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c3cac-137">-StartTime</span></span>
<span data-ttu-id="c3cac-138">업로드할 서비스 로그의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="c3cac-139">-확인</span><span class="sxs-lookup"><span data-stu-id="c3cac-139">-Confirm</span></span>
<span data-ttu-id="c3cac-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cac-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cac-141">-WhatIf</span></span>
<span data-ttu-id="c3cac-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3cac-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cac-144">CommonParameters</span></span>
<span data-ttu-id="c3cac-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3cac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cac-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cac-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cac-147">입력</span><span class="sxs-lookup"><span data-stu-id="c3cac-147">INPUTS</span></span>

### <span data-ttu-id="c3cac-148">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3cac-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="c3cac-149">매개 변수: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3cac-149">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="c3cac-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3cac-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c3cac-151">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3cac-151">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c3cac-152">출력</span><span class="sxs-lookup"><span data-stu-id="c3cac-152">OUTPUTS</span></span>

### <span data-ttu-id="c3cac-153">Microsoft.Azure.Commands.Batch. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="c3cac-153">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="c3cac-154">상속자</span><span class="sxs-lookup"><span data-stu-id="c3cac-154">NOTES</span></span>

## <span data-ttu-id="c3cac-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3cac-155">RELATED LINKS</span></span>
