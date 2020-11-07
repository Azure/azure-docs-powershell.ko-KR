---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 4581cfea88982eee4144730b92662374ec0a5790
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698487"
---
# <span data-ttu-id="37679-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="37679-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="37679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37679-102">SYNOPSIS</span></span>
<span data-ttu-id="37679-103">이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37679-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="37679-104">이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37679-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="37679-105">구문과</span><span class="sxs-lookup"><span data-stu-id="37679-105">SYNTAX</span></span>

### <span data-ttu-id="37679-106">ObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="37679-106">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37679-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="37679-107">StringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37679-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="37679-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37679-109">설명은</span><span class="sxs-lookup"><span data-stu-id="37679-109">DESCRIPTION</span></span>
<span data-ttu-id="37679-110">이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37679-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="37679-111">이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37679-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="37679-112">동기화 그룹의 다른 끝점에 이미 파일이 있고 새로 추가 된 위치에도 파일이 포함 되어 있는 경우 조정 프로세스는 다른 끝점에서와 동일한 폴더의 파일이 실제로 같은지 여부를 확인 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="37679-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="37679-113">네임 스페이스는 병합 및 조정을 통해 충돌 하는 파일을 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37679-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="37679-114">다른 서버 끝점에 파일이 있는 경우이 서버에서 빈 위치를 시작 하는 것이 더 좋을 수 있으며, 이렇게 하면 클라우드의 파일이 빠른 재해 복구 라는 자동 프로세스로 서버에 도달 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37679-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="37679-115">네임 스페이스 메타 데이터는 먼저 동기화 되므로 각 파일의 데이터 스트림은 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37679-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="37679-116">사용자 또는 응용 프로그램이 다운로드 순서를 초과 하 여 파일을 요청 하는 경우 해당 파일은 액세스 요청을 충족 하기 위해 우선 순위로 회수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37679-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="37679-117">선택적으로이 서버 끝점에서 클라우드 계층화를 사용 하 여이 끝점이 클라우드의 전체 파일 집합에 대 한 캐시 인지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37679-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="37679-118">클라우드 계층화를 사용 하는 경우 설정할 수 있는 클라우드 계층화 정책에 정의 된 지점에서 파일 콘텐츠 다운로드가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37679-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="37679-119">예제의</span><span class="sxs-lookup"><span data-stu-id="37679-119">EXAMPLES</span></span>

### <span data-ttu-id="37679-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="37679-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="37679-121">이 명령은 등록 된 서버에서 새 서버 끝점을 만들어 동기화 그룹에 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="37679-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="37679-122">이 방법은 다른 끝점의 토폴로지에 포함 되며 파일 메타 데이터와 콘텐츠가 동기화 그룹의 끝점으로 참조 되는 모든 위치 간에 즉시 동기화 되기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37679-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="37679-123">변수</span><span class="sxs-lookup"><span data-stu-id="37679-123">PARAMETERS</span></span>

### <span data-ttu-id="37679-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37679-124">-AsJob</span></span>
<span data-ttu-id="37679-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="37679-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37679-126">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="37679-126">-OfflineDataTransfer</span></span>
<span data-ttu-id="37679-127">클라우드 시드 데이터 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37679-127">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="37679-128">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="37679-128">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="37679-129">클라우드 시드 데이터 파일 공유 Uri 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37679-129">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="37679-130">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="37679-130">-CloudTiering</span></span>
<span data-ttu-id="37679-131">클라우드 Tiering 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37679-131">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="37679-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37679-132">-DefaultProfile</span></span>
<span data-ttu-id="37679-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37679-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37679-134">-이름</span><span class="sxs-lookup"><span data-stu-id="37679-134">-Name</span></span>
<span data-ttu-id="37679-135">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37679-135">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="37679-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37679-136">-ParentObject</span></span>
<span data-ttu-id="37679-137">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37679-137">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="37679-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="37679-138">-ParentResourceId</span></span>
<span data-ttu-id="37679-139">SyncGroup 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="37679-139">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="37679-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37679-140">-ResourceGroupName</span></span>
<span data-ttu-id="37679-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37679-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="37679-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="37679-142">-ServerLocalPath</span></span>
<span data-ttu-id="37679-143">서버 로컬 경로 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37679-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="37679-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="37679-144">-ServerResourceId</span></span>
<span data-ttu-id="37679-145">RegisteredServer 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="37679-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="37679-146">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="37679-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="37679-147">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37679-147">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="37679-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="37679-148">-SyncGroupName</span></span>
<span data-ttu-id="37679-149">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37679-149">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="37679-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="37679-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="37679-151">일 보다 오래 된 계층 파일 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37679-151">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="37679-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="37679-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="37679-153">볼륨 사용 가능한 공간 백분율 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37679-153">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="37679-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37679-154">CommonParameters</span></span>
<span data-ttu-id="37679-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37679-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37679-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37679-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37679-157">입력</span><span class="sxs-lookup"><span data-stu-id="37679-157">INPUTS</span></span>

### <span data-ttu-id="37679-158">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="37679-158">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="37679-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37679-159">System.String</span></span>

## <span data-ttu-id="37679-160">출력</span><span class="sxs-lookup"><span data-stu-id="37679-160">OUTPUTS</span></span>

### <span data-ttu-id="37679-161">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="37679-161">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="37679-162">상속자</span><span class="sxs-lookup"><span data-stu-id="37679-162">NOTES</span></span>

## <span data-ttu-id="37679-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37679-163">RELATED LINKS</span></span>
