---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198489"
---
# <span data-ttu-id="7876d-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="7876d-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="7876d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7876d-102">SYNOPSIS</span></span>
<span data-ttu-id="7876d-103">Storage 계정의 장애 조치(failover)를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="7876d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7876d-104">SYNTAX</span></span>

### <span data-ttu-id="7876d-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7876d-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7876d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7876d-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7876d-107">설명</span><span class="sxs-lookup"><span data-stu-id="7876d-107">DESCRIPTION</span></span>
<span data-ttu-id="7876d-108">Storage 계정의 장애 조치(failover)를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="7876d-109">가용성 문제가 있는 경우 저장소 계정에 대해 장애 조치 요청을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="7876d-110">장애 조치는 저장소 계정의 주 클러스터에서 RA-GRS 계정에 대한 보조 클러스터로 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="7876d-111">장애 조치(failover) 후 보조 클러스터가 주 클러스터가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="7876d-112">장애 조치(failover)를 시작하기 전에 저장소 계정에 미치는 영향은 1.1입니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="7876d-113">계정에 대해 GET Blob Service 통계(, GET Table Service 통계( 및 GET Queue Service 통계)를 사용하여 마지막 동기화 https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) 시간을 https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="7876d-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="7876d-114">장애 조치(failover)를 시작하면 손실될 수 있는 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="7876d-115">2.장애 조치(failover) 후 저장소 계정 유형은 LRS(로컬 중복 저장소)로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="7876d-116">GRS(지역 중복 저장소)를 사용하려면 계정을 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="7876d-117">3. 저장소 계정에 대해 GRS를 다시 사용하도록 설정하면 Microsoft는 새 보조 지역에 데이터를 복제합니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="7876d-118">복제 시간은 복제할 데이터의 양에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="7876d-119">부트스트락에 대한 대역폭 요금이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="7876d-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="7876d-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="7876d-121">예제</span><span class="sxs-lookup"><span data-stu-id="7876d-121">EXAMPLES</span></span>

### <span data-ttu-id="7876d-122">예제 1: Storage 계정의 장애 조치(failover) 호출</span><span class="sxs-lookup"><span data-stu-id="7876d-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="7876d-123">이 명령은 Storage 계정의 마지막 동기화 시간을 확인한 다음, 해당 계정의 장애 조치(failover)를 호출하고, 장애 조치(failover) 후 보조 클러스터가 주 클러스터가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="7876d-124">장애 조치(failover)에 시간이 오래 걸리기 때문에 -Asjob 매개 변수를 사용하여 백엔드에서 실행한 다음 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="7876d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7876d-125">PARAMETERS</span></span>

### <span data-ttu-id="7876d-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7876d-126">-AsJob</span></span>
<span data-ttu-id="7876d-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7876d-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7876d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7876d-128">-DefaultProfile</span></span>
<span data-ttu-id="7876d-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7876d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="7876d-130">-Force</span></span>
<span data-ttu-id="7876d-131">강제로 계정을 장애 조치(failover)합니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="7876d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7876d-132">-InputObject</span></span>
<span data-ttu-id="7876d-133">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="7876d-133">Storage account object</span></span>

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

### <span data-ttu-id="7876d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7876d-134">-Name</span></span>
<span data-ttu-id="7876d-135">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="7876d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7876d-136">-ResourceGroupName</span></span>
<span data-ttu-id="7876d-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="7876d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7876d-138">-Confirm</span></span>
<span data-ttu-id="7876d-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7876d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7876d-140">-WhatIf</span></span>
<span data-ttu-id="7876d-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7876d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7876d-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7876d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7876d-143">CommonParameters</span></span>
<span data-ttu-id="7876d-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7876d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7876d-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7876d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7876d-146">입력</span><span class="sxs-lookup"><span data-stu-id="7876d-146">INPUTS</span></span>

### <span data-ttu-id="7876d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7876d-147">System.String</span></span>

## <span data-ttu-id="7876d-148">출력</span><span class="sxs-lookup"><span data-stu-id="7876d-148">OUTPUTS</span></span>

### <span data-ttu-id="7876d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7876d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7876d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7876d-150">NOTES</span></span>

## <span data-ttu-id="7876d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7876d-151">RELATED LINKS</span></span>
