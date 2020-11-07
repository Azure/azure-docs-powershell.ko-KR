---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 03b4ea18bc40f8ddd3a2dc2605427013c45d7506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698470"
---
# <span data-ttu-id="efbc6-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="efbc6-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="efbc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="efbc6-103">이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="efbc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efbc6-104">SYNTAX</span></span>

### <span data-ttu-id="efbc6-105">ObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="efbc6-105">ObjectParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efbc6-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="efbc6-106">StringParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efbc6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efbc6-107">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efbc6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="efbc6-108">DESCRIPTION</span></span>
<span data-ttu-id="efbc6-109">이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="efbc6-110">예를 들어 클라우드 계층 및 클라우드 계층화 정책은 언제 든 지 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="efbc6-111">서버 끝점을 만든 후 로컬 경로와 같은 서버 끝점의 여러 측면을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="efbc6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="efbc6-112">EXAMPLES</span></span>

### <span data-ttu-id="efbc6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="efbc6-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="efbc6-114">이 예제에서는 두 가지 작업을 수행 하 고, 지난 30 일 동안 액세스 되지 않은 모든 파일을 서버에 게 지정 하 고, 생성 중에이 서버 끝점에서 처음으로 사용 하도록 설정 된 오프 라인 데이터 전송 모드를 사용 하지 않도록 설정 하는 새 클라우드 계층화 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="efbc6-115">오프 라인 데이터 전송은 Azure 데이터 상자와 같은 대량 마이그레이션 서비스와의 상호 운용성의 일부로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="efbc6-116">변수</span><span class="sxs-lookup"><span data-stu-id="efbc6-116">PARAMETERS</span></span>

### <span data-ttu-id="efbc6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efbc6-117">-AsJob</span></span>
<span data-ttu-id="efbc6-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="efbc6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efbc6-119">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="efbc6-119">-OfflineDataTransfer</span></span>
<span data-ttu-id="efbc6-120">클라우드 시드 데이터 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efbc6-120">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="efbc6-121">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="efbc6-121">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="efbc6-122">클라우드 시드 데이터 파일 공유 Uri 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efbc6-122">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="efbc6-123">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="efbc6-123">-CloudTiering</span></span>
<span data-ttu-id="efbc6-124">클라우드 Tiering 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efbc6-124">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="efbc6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbc6-125">-DefaultProfile</span></span>
<span data-ttu-id="efbc6-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efbc6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efbc6-127">-InputObject</span></span>
<span data-ttu-id="efbc6-128">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-128">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="efbc6-129">-이름</span><span class="sxs-lookup"><span data-stu-id="efbc6-129">-Name</span></span>
<span data-ttu-id="efbc6-130">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-130">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="efbc6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efbc6-131">-ResourceGroupName</span></span>
<span data-ttu-id="efbc6-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="efbc6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efbc6-133">-ResourceId</span></span>
<span data-ttu-id="efbc6-134">ServerEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="efbc6-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="efbc6-135">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="efbc6-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="efbc6-136">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="efbc6-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="efbc6-137">-SyncGroupName</span></span>
<span data-ttu-id="efbc6-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="efbc6-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="efbc6-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="efbc6-140">일 보다 오래 된 계층 파일 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efbc6-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="efbc6-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="efbc6-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="efbc6-142">볼륨 사용 가능한 공간 백분율 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efbc6-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="efbc6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbc6-143">CommonParameters</span></span>
<span data-ttu-id="efbc6-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efbc6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbc6-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbc6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbc6-146">입력</span><span class="sxs-lookup"><span data-stu-id="efbc6-146">INPUTS</span></span>

### <span data-ttu-id="efbc6-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="efbc6-147">System.String</span></span>

### <span data-ttu-id="efbc6-148">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="efbc6-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="efbc6-149">출력</span><span class="sxs-lookup"><span data-stu-id="efbc6-149">OUTPUTS</span></span>

### <span data-ttu-id="efbc6-150">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="efbc6-150">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="efbc6-151">상속자</span><span class="sxs-lookup"><span data-stu-id="efbc6-151">NOTES</span></span>

## <span data-ttu-id="efbc6-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efbc6-152">RELATED LINKS</span></span>
