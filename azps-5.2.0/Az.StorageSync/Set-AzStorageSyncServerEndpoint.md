---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366556"
---
# <span data-ttu-id="ac040-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac040-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ac040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac040-102">SYNOPSIS</span></span>
<span data-ttu-id="ac040-103">이 명령을 사용하면 서버 엔드포인트의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="ac040-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac040-104">SYNTAX</span></span>

### <span data-ttu-id="ac040-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac040-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac040-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac040-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac040-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac040-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac040-108">설명</span><span class="sxs-lookup"><span data-stu-id="ac040-108">DESCRIPTION</span></span>
<span data-ttu-id="ac040-109">이 명령을 사용하면 서버 엔드포인트의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="ac040-110">예를 들어 클라우드 계층화 및 클라우드 계층화 정책은 수시로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="ac040-111">서버 엔드포인트를 만든 후에 로컬 경로와 같은 서버 엔드포인트의 여러 측면을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="ac040-112">예제</span><span class="sxs-lookup"><span data-stu-id="ac040-112">EXAMPLES</span></span>

### <span data-ttu-id="ac040-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac040-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="ac040-114">이 예제에서는 지정된 서버 엔드포인트에 새 클라우드 계층화 정책을 설정하여 지난 30일 동안 액세스하지 않은 모든 파일을 서버가 계층화하고 오프라인 데이터 전송 모드도 사용하지 않도록 설정하며, 이 작업은 생성 중에 이 서버 엔드포인트에서 처음 사용하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="ac040-115">오프라인 데이터 전송은 Azure Data Box와 같은 대량 마이그레이션 서비스와의 상호운용성의 일부로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="ac040-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac040-116">PARAMETERS</span></span>

### <span data-ttu-id="ac040-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac040-117">-AsJob</span></span>
<span data-ttu-id="ac040-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ac040-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac040-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="ac040-119">-CloudTiering</span></span>
<span data-ttu-id="ac040-120">클라우드 계층화 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac040-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="ac040-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac040-121">-DefaultProfile</span></span>
<span data-ttu-id="ac040-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac040-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac040-123">-InputObject</span></span>
<span data-ttu-id="ac040-124">일반적으로 매개 변수를 통해 전달되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac040-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ac040-125">-Name</span></span>
<span data-ttu-id="ac040-126">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac040-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="ac040-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="ac040-128">클라우드 시드 데이터 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac040-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="ac040-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="ac040-129">-localCacheMode</span></span>
<span data-ttu-id="ac040-130">로컬 캐시 모드 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac040-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="ac040-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac040-131">-ResourceGroupName</span></span>
<span data-ttu-id="ac040-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac040-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac040-133">-ResourceId</span></span>
<span data-ttu-id="ac040-134">ServerEndpoint 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ac040-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac040-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ac040-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="ac040-136">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac040-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ac040-137">-SyncGroupName</span></span>
<span data-ttu-id="ac040-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac040-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ac040-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="ac040-140">일보다 오래된 계층 파일 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac040-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="ac040-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="ac040-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="ac040-142">볼륨 사용 공간 백분율 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac040-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="ac040-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac040-143">-Confirm</span></span>
<span data-ttu-id="ac040-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac040-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac040-145">-WhatIf</span></span>
<span data-ttu-id="ac040-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ac040-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac040-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac040-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac040-148">CommonParameters</span></span>
<span data-ttu-id="ac040-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac040-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac040-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ac040-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac040-151">입력</span><span class="sxs-lookup"><span data-stu-id="ac040-151">INPUTS</span></span>

### <span data-ttu-id="ac040-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ac040-152">System.String</span></span>

### <span data-ttu-id="ac040-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac040-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ac040-154">출력</span><span class="sxs-lookup"><span data-stu-id="ac040-154">OUTPUTS</span></span>

### <span data-ttu-id="ac040-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac040-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="ac040-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac040-156">NOTES</span></span>

## <span data-ttu-id="ac040-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac040-157">RELATED LINKS</span></span>
