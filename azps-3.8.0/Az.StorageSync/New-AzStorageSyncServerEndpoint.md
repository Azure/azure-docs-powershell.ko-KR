---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: c21ea8d0dedef5afda6c8f40eedf949b915f0367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043123"
---
# <span data-ttu-id="8ae33-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ae33-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="8ae33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ae33-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae33-103">이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="8ae33-104">이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="8ae33-105">구문과</span><span class="sxs-lookup"><span data-stu-id="8ae33-105">SYNTAX</span></span>

### <span data-ttu-id="8ae33-106">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ae33-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae33-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ae33-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae33-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ae33-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ae33-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8ae33-109">DESCRIPTION</span></span>
<span data-ttu-id="8ae33-110">이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="8ae33-111">이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="8ae33-112">동기화 그룹의 다른 끝점에 이미 파일이 있고 새로 추가 된 위치에도 파일이 포함 되어 있는 경우 조정 프로세스는 다른 끝점에서와 동일한 폴더의 파일이 실제로 같은지 여부를 확인 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="8ae33-113">네임 스페이스는 병합 및 조정을 통해 충돌 하는 파일을 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="8ae33-114">다른 서버 끝점에 파일이 있는 경우이 서버에서 빈 위치를 시작 하는 것이 더 좋을 수 있으며, 이렇게 하면 클라우드의 파일이 빠른 재해 복구 라는 자동 프로세스로 서버에 도달 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="8ae33-115">네임 스페이스 메타 데이터는 먼저 동기화 되므로 각 파일의 데이터 스트림은 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="8ae33-116">사용자 또는 응용 프로그램이 다운로드 순서를 초과 하 여 파일을 요청 하는 경우 해당 파일은 액세스 요청을 충족 하기 위해 우선 순위로 회수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="8ae33-117">선택적으로이 서버 끝점에서 클라우드 계층화를 사용 하 여이 끝점이 클라우드의 전체 파일 집합에 대 한 캐시 인지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="8ae33-118">클라우드 계층화를 사용 하는 경우 설정할 수 있는 클라우드 계층화 정책에 정의 된 지점에서 파일 콘텐츠 다운로드가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="8ae33-119">예제의</span><span class="sxs-lookup"><span data-stu-id="8ae33-119">EXAMPLES</span></span>

### <span data-ttu-id="8ae33-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ae33-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="8ae33-121">이 명령은 등록 된 서버에서 새 서버 끝점을 만들어 동기화 그룹에 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="8ae33-122">이 방법은 다른 끝점의 토폴로지에 포함 되며 파일 메타 데이터와 콘텐츠가 동기화 그룹의 끝점으로 참조 되는 모든 위치 간에 즉시 동기화 되기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="8ae33-123">변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-123">PARAMETERS</span></span>

### <span data-ttu-id="8ae33-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae33-124">-AsJob</span></span>
<span data-ttu-id="8ae33-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8ae33-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ae33-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="8ae33-126">-CloudTiering</span></span>
<span data-ttu-id="8ae33-127">클라우드 Tiering 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="8ae33-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae33-128">-DefaultProfile</span></span>
<span data-ttu-id="8ae33-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ae33-130">-이름</span><span class="sxs-lookup"><span data-stu-id="8ae33-130">-Name</span></span>
<span data-ttu-id="8ae33-131">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae33-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="8ae33-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="8ae33-133">클라우드 시드 데이터 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="8ae33-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="8ae33-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="8ae33-135">클라우드 시드 데이터 파일 공유 Uri 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="8ae33-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8ae33-136">-ParentObject</span></span>
<span data-ttu-id="8ae33-137">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-137">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae33-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8ae33-138">-ParentResourceId</span></span>
<span data-ttu-id="8ae33-139">SyncGroup 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8ae33-139">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae33-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae33-140">-ResourceGroupName</span></span>
<span data-ttu-id="8ae33-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ae33-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="8ae33-142">-ServerLocalPath</span></span>
<span data-ttu-id="8ae33-143">서버 로컬 경로 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="8ae33-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="8ae33-144">-ServerResourceId</span></span>
<span data-ttu-id="8ae33-145">RegisteredServer 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8ae33-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="8ae33-146">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="8ae33-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="8ae33-147">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-147">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8ae33-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae33-148">-SyncGroupName</span></span>
<span data-ttu-id="8ae33-149">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-149">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="8ae33-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="8ae33-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="8ae33-151">일 보다 오래 된 계층 파일 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-151">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="8ae33-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="8ae33-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="8ae33-153">볼륨 사용 가능한 공간 백분율 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae33-153">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="8ae33-154">-확인</span><span class="sxs-lookup"><span data-stu-id="8ae33-154">-Confirm</span></span>
<span data-ttu-id="8ae33-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae33-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae33-156">-WhatIf</span></span>
<span data-ttu-id="8ae33-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ae33-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae33-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae33-159">CommonParameters</span></span>
<span data-ttu-id="8ae33-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae33-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae33-161">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae33-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae33-162">입력</span><span class="sxs-lookup"><span data-stu-id="8ae33-162">INPUTS</span></span>

### <span data-ttu-id="8ae33-163">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="8ae33-163">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="8ae33-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ae33-164">System.String</span></span>

## <span data-ttu-id="8ae33-165">출력</span><span class="sxs-lookup"><span data-stu-id="8ae33-165">OUTPUTS</span></span>

### <span data-ttu-id="8ae33-166">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ae33-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="8ae33-167">상속자</span><span class="sxs-lookup"><span data-stu-id="8ae33-167">NOTES</span></span>

## <span data-ttu-id="8ae33-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ae33-168">RELATED LINKS</span></span>