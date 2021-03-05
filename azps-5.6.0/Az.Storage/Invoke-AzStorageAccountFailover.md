---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: c2dd4abcf9e917d4a34ed548cd356e02875971b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994770"
---
# <span data-ttu-id="c69c8-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="c69c8-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="c69c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c69c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c69c8-103">Storage 계정의 장애 조치(failover)를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="c69c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="c69c8-104">SYNTAX</span></span>

### <span data-ttu-id="c69c8-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c69c8-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c69c8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c69c8-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c69c8-107">설명</span><span class="sxs-lookup"><span data-stu-id="c69c8-107">DESCRIPTION</span></span>
<span data-ttu-id="c69c8-108">Storage 계정의 장애 조치(failover)를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="c69c8-109">가용성 문제가 있는 경우 저장소 계정에 대해 장애 조치(Failover) 요청을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="c69c8-110">장애 조치(failover)는 스토리지 계정의 주 클러스터에서 RA-GRS 계정에 대한 보조 클러스터로 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="c69c8-111">장애 조치(failover) 후 보조 클러스터가 기본 클러스터가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="c69c8-112">장애 조치(failover)를 시작하기 전에 저장소 계정에 미치는 영향은 1.1입니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="c69c8-113">GET Blob Service 통계(, GET Table ServiceStats) 및 GET Queue Service 통계(계정의 경우)를 사용하여 마지막 동기화 시간을 https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats) https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="c69c8-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="c69c8-114">장애 조치(failover)를 시작하면 손실될 수 있는 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="c69c8-115">2.장애 조치(failover) 후 저장소 계정 유형이 LRS(로컬 중복 저장소)로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="c69c8-116">GRS(지역 중복 저장소)를 사용하기 위해 계정을 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="c69c8-117">3.저장소 계정에 GRS를 다시 사용하도록 설정하면 Microsoft는 데이터를 새 보조 지역에 복제합니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="c69c8-118">복제 시간은 복제할 데이터의 양에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="c69c8-119">부트스트레이프에 대한 대역폭 요금이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="c69c8-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="c69c8-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="c69c8-121">예제</span><span class="sxs-lookup"><span data-stu-id="c69c8-121">EXAMPLES</span></span>

### <span data-ttu-id="c69c8-122">예제 1: Storage 계정의 장애 조치(failover)를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="c69c8-123">이 명령은 Storage 계정의 마지막 동기화 시간을 확인한 다음 장애 조치(failover)를 호출하고 장애 조치(failover) 후 보조 클러스터가 주 클러스터가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="c69c8-124">장애 조치(failover)에는 시간이 오래 걸리기 때문에 -Asjob 매개 변수를 사용하여 백엔드에서 실행한 다음 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="c69c8-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c69c8-125">PARAMETERS</span></span>

### <span data-ttu-id="c69c8-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c69c8-126">-AsJob</span></span>
<span data-ttu-id="c69c8-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c69c8-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c69c8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69c8-128">-DefaultProfile</span></span>
<span data-ttu-id="c69c8-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c69c8-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c69c8-130">-Force</span></span>
<span data-ttu-id="c69c8-131">계정 장애 조치(Failover)를 강제로 설정</span><span class="sxs-lookup"><span data-stu-id="c69c8-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="c69c8-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c69c8-132">-InputObject</span></span>
<span data-ttu-id="c69c8-133">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c69c8-133">Storage account object</span></span>

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

### <span data-ttu-id="c69c8-134">-Name</span><span class="sxs-lookup"><span data-stu-id="c69c8-134">-Name</span></span>
<span data-ttu-id="c69c8-135">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="c69c8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69c8-136">-ResourceGroupName</span></span>
<span data-ttu-id="c69c8-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="c69c8-138">-확인</span><span class="sxs-lookup"><span data-stu-id="c69c8-138">-Confirm</span></span>
<span data-ttu-id="c69c8-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c69c8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c69c8-140">-WhatIf</span></span>
<span data-ttu-id="c69c8-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c69c8-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c69c8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69c8-143">CommonParameters</span></span>
<span data-ttu-id="c69c8-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c69c8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69c8-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c69c8-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69c8-146">입력</span><span class="sxs-lookup"><span data-stu-id="c69c8-146">INPUTS</span></span>

### <span data-ttu-id="c69c8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c69c8-147">System.String</span></span>

## <span data-ttu-id="c69c8-148">출력</span><span class="sxs-lookup"><span data-stu-id="c69c8-148">OUTPUTS</span></span>

### <span data-ttu-id="c69c8-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c69c8-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c69c8-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c69c8-150">NOTES</span></span>

## <span data-ttu-id="c69c8-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c69c8-151">RELATED LINKS</span></span>
