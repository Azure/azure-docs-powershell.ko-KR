---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212078"
---
# <span data-ttu-id="617e0-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="617e0-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="617e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="617e0-102">SYNOPSIS</span></span>
<span data-ttu-id="617e0-103">저장소 계정의 장애 조치 (failover)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="617e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="617e0-104">SYNTAX</span></span>

### <span data-ttu-id="617e0-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="617e0-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617e0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="617e0-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="617e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="617e0-107">DESCRIPTION</span></span>
<span data-ttu-id="617e0-108">저장소 계정의 장애 조치 (failover)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="617e0-109">가용성 문제가 발생 하는 경우 저장소 계정에 대 한 장애 조치 요청이 트리거될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="617e0-110">저장소 계정의 기본 클러스터에서 RA-GRS 계정에 대 한 보조 클러스터로 장애 조치 (failover)가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="617e0-111">보조 클러스터는 장애 조치 후에 기본으로 됩니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="617e0-112">장애 조치 (failover)를 시작 하기 전에 저장소 계정에 대 한 다음 영향을 이해 하십시오. 1.1.</span><span class="sxs-lookup"><span data-stu-id="617e0-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="617e0-113">Blob 가져오기 서비스 통계를 사용 하 여 마지막 동기화 시간을 확인 하세요 ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) 계정에 대 한 테이블 서비스 통계 가져오기 https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) 및 큐 서비스 통계 가져오기) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) .</span><span class="sxs-lookup"><span data-stu-id="617e0-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="617e0-114">장애 조치를 시작 하는 경우 손실 될 수 있는 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="617e0-115">2. 장애 조치 (failover) 후 저장소 계정 유형이 로컬 중복 저장소 (LRS)로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="617e0-116">GRS (지역 중복 저장소)를 사용 하도록 계정을 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="617e0-117">3. 저장소 계정에 대 한 GRS을 다시 사용 하도록 설정 하면 Microsoft에서 새 보조 지역으로 데이터를 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="617e0-118">복제 시간은 복제할 데이터 양에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="617e0-119">부트스트랩에 대 한 대역폭 요금은에는 없다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="617e0-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="617e0-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="617e0-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="617e0-121">예제의</span><span class="sxs-lookup"><span data-stu-id="617e0-121">EXAMPLES</span></span>

### <span data-ttu-id="617e0-122">예제 1: 저장소 계정의 장애 조치 (failover) 호출</span><span class="sxs-lookup"><span data-stu-id="617e0-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="617e0-123">이 명령은 저장소 계정의 마지막 동기화 시간을 확인 한 후 장애 조치를 실행 하 여 장애 조치 후 보조 클러스터가 기본으로 됩니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="617e0-124">장애 조치 (failover)는 시간이 오래 걸리기 때문에-Asjob 매개 변수를 사용 하 여 백엔드에서 실행 하는 것을 제안 하 고 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="617e0-125">변수</span><span class="sxs-lookup"><span data-stu-id="617e0-125">PARAMETERS</span></span>

### <span data-ttu-id="617e0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="617e0-126">-AsJob</span></span>
<span data-ttu-id="617e0-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="617e0-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="617e0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617e0-128">-DefaultProfile</span></span>
<span data-ttu-id="617e0-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="617e0-130">-Force</span><span class="sxs-lookup"><span data-stu-id="617e0-130">-Force</span></span>
<span data-ttu-id="617e0-131">계정을 강제로 장애 조치 (Failover)</span><span class="sxs-lookup"><span data-stu-id="617e0-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="617e0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="617e0-132">-InputObject</span></span>
<span data-ttu-id="617e0-133">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="617e0-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="617e0-134">-이름</span><span class="sxs-lookup"><span data-stu-id="617e0-134">-Name</span></span>
<span data-ttu-id="617e0-135">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617e0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617e0-136">-ResourceGroupName</span></span>
<span data-ttu-id="617e0-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="617e0-138">-확인</span><span class="sxs-lookup"><span data-stu-id="617e0-138">-Confirm</span></span>
<span data-ttu-id="617e0-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="617e0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617e0-140">-WhatIf</span></span>
<span data-ttu-id="617e0-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="617e0-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="617e0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617e0-143">CommonParameters</span></span>
<span data-ttu-id="617e0-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="617e0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617e0-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="617e0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617e0-146">입력</span><span class="sxs-lookup"><span data-stu-id="617e0-146">INPUTS</span></span>

### <span data-ttu-id="617e0-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="617e0-147">System.String</span></span>

## <span data-ttu-id="617e0-148">출력</span><span class="sxs-lookup"><span data-stu-id="617e0-148">OUTPUTS</span></span>

### <span data-ttu-id="617e0-149">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="617e0-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="617e0-150">상속자</span><span class="sxs-lookup"><span data-stu-id="617e0-150">NOTES</span></span>

## <span data-ttu-id="617e0-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="617e0-151">RELATED LINKS</span></span>
