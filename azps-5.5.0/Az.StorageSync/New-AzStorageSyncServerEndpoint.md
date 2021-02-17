---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195665"
---
# <span data-ttu-id="d1e43-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1e43-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="d1e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1e43-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e43-103">이 명령은 등록된 서버에 새 서버 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="d1e43-104">이렇게 하면 서버의 지정된 경로가 동기화 그룹의 다른 엔드포인트와 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="d1e43-105">구문</span><span class="sxs-lookup"><span data-stu-id="d1e43-105">SYNTAX</span></span>

### <span data-ttu-id="d1e43-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1e43-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e43-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e43-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e43-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e43-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e43-109">설명</span><span class="sxs-lookup"><span data-stu-id="d1e43-109">DESCRIPTION</span></span>
<span data-ttu-id="d1e43-110">이 명령은 등록된 서버에 새 서버 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="d1e43-111">이렇게 하면 서버의 지정된 경로가 동기화 그룹의 다른 엔드포인트와 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="d1e43-112">동기화 그룹의 다른 엔드포인트에 이미 파일이 있으며 새로 추가된 위치에도 파일이 포함되어 있는 경우, 화해 프로세스는 파일이 실제로 다른 엔드포인트와 동일한 폴더에 있는지 확인하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="d1e43-113">네임스페이스는 병합 및 해결을 통해 충돌 파일을 방지하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="d1e43-114">다른 서버 엔드포인트에 파일이 있는 경우 클라우드의 파일이 빠른 재해 복구라는 자동 프로세스에서 서버로 이동하기 위해 이 서버의 빈 위치로 시작하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="d1e43-115">네임스페이스 메타데이터가 먼저 동기화된 다음 각 파일의 데이터 스트림이 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="d1e43-116">사용자 또는 애플리케이션이 다운로드 순서를 어서 파일을 요청하는 경우 해당 파일은 액세스 요청을 충족하기 위해 우선 순위에 따라 회수됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="d1e43-117">선택적으로 이 서버 엔드포인트에서 클라우드 계층을 사용하여 이 엔드포인트가 클라우드의 전체 파일 집합의 캐시가 되기로 해야 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="d1e43-118">클라우드 계층화가 사용되는 경우 설정할 수 있는 클라우드 계층화 정책에 정의된 지점에서 파일 콘텐츠 다운로드가 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="d1e43-119">예제</span><span class="sxs-lookup"><span data-stu-id="d1e43-119">EXAMPLES</span></span>

### <span data-ttu-id="d1e43-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1e43-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="d1e43-121">이 명령은 등록된 서버에 새 서버 엔드포인트를 만들고 동기화 그룹에 삽입합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="d1e43-122">다른 엔드포인트 및 파일 메타데이터 및 콘텐츠의 토폴로지의 일부인 THis 방식은 동기화 그룹의 엔드포인트로 참조되는 모든 위치 간에 즉시 동기화를 시작하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="d1e43-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1e43-123">PARAMETERS</span></span>

### <span data-ttu-id="d1e43-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1e43-124">-AsJob</span></span>
<span data-ttu-id="d1e43-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d1e43-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1e43-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="d1e43-126">-CloudTiering</span></span>
<span data-ttu-id="d1e43-127">클라우드 계층화 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="d1e43-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e43-128">-DefaultProfile</span></span>
<span data-ttu-id="d1e43-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e43-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d1e43-130">-Name</span></span>
<span data-ttu-id="d1e43-131">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="d1e43-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="d1e43-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="d1e43-133">클라우드 시드 데이터 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="d1e43-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="d1e43-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="d1e43-135">클라우드 시드 데이터 파일 공유 URI 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="d1e43-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="d1e43-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="d1e43-137">로컬 캐시 모드 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="d1e43-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="d1e43-138">-localCacheMode</span></span>
<span data-ttu-id="d1e43-139">로컬 캐시 모드 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="d1e43-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1e43-140">-ParentObject</span></span>
<span data-ttu-id="d1e43-141">일반적으로 매개 변수를 통해 전달되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d1e43-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e43-142">-ParentResourceId</span></span>
<span data-ttu-id="d1e43-143">SyncGroup 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d1e43-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="d1e43-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e43-144">-ResourceGroupName</span></span>
<span data-ttu-id="d1e43-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="d1e43-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="d1e43-146">-ServerLocalPath</span></span>
<span data-ttu-id="d1e43-147">서버 로컬 경로 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="d1e43-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e43-148">-ServerResourceId</span></span>
<span data-ttu-id="d1e43-149">RegisteredServer 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d1e43-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="d1e43-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d1e43-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="d1e43-151">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d1e43-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e43-152">-SyncGroupName</span></span>
<span data-ttu-id="d1e43-153">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d1e43-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="d1e43-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="d1e43-155">일보다 오래된 계층 파일 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="d1e43-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="d1e43-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="d1e43-157">볼륨 사용 공간 백분율 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1e43-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="d1e43-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1e43-158">-Confirm</span></span>
<span data-ttu-id="d1e43-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e43-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e43-160">-WhatIf</span></span>
<span data-ttu-id="d1e43-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d1e43-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1e43-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e43-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e43-163">CommonParameters</span></span>
<span data-ttu-id="d1e43-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e43-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e43-165">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1e43-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e43-166">입력</span><span class="sxs-lookup"><span data-stu-id="d1e43-166">INPUTS</span></span>

### <span data-ttu-id="d1e43-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d1e43-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="d1e43-168">System.String</span><span class="sxs-lookup"><span data-stu-id="d1e43-168">System.String</span></span>

## <span data-ttu-id="d1e43-169">출력</span><span class="sxs-lookup"><span data-stu-id="d1e43-169">OUTPUTS</span></span>

### <span data-ttu-id="d1e43-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1e43-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="d1e43-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1e43-171">NOTES</span></span>

## <span data-ttu-id="d1e43-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1e43-172">RELATED LINKS</span></span>
