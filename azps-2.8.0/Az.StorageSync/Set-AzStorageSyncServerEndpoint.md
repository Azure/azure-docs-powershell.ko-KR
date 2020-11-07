---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 23aab4561e8127c67be4d9f751b250bc3fb6d1a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871997"
---
# <span data-ttu-id="883ba-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="883ba-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="883ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="883ba-102">SYNOPSIS</span></span>
<span data-ttu-id="883ba-103">이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="883ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="883ba-104">SYNTAX</span></span>

### <span data-ttu-id="883ba-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="883ba-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883ba-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="883ba-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883ba-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="883ba-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="883ba-108">설명은</span><span class="sxs-lookup"><span data-stu-id="883ba-108">DESCRIPTION</span></span>
<span data-ttu-id="883ba-109">이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="883ba-110">예를 들어 클라우드 계층 및 클라우드 계층화 정책은 언제 든 지 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="883ba-111">서버 끝점을 만든 후 로컬 경로와 같은 서버 끝점의 여러 측면을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="883ba-112">예제의</span><span class="sxs-lookup"><span data-stu-id="883ba-112">EXAMPLES</span></span>

### <span data-ttu-id="883ba-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="883ba-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="883ba-114">이 예제에서는 두 가지 작업을 수행 하 고, 지난 30 일 동안 액세스 되지 않은 모든 파일을 서버에 게 지정 하 고, 생성 중에이 서버 끝점에서 처음으로 사용 하도록 설정 된 오프 라인 데이터 전송 모드를 사용 하지 않도록 설정 하는 새 클라우드 계층화 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="883ba-115">오프 라인 데이터 전송은 Azure 데이터 상자와 같은 대량 마이그레이션 서비스와의 상호 운용성의 일부로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="883ba-116">변수</span><span class="sxs-lookup"><span data-stu-id="883ba-116">PARAMETERS</span></span>

### <span data-ttu-id="883ba-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="883ba-117">-AsJob</span></span>
<span data-ttu-id="883ba-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="883ba-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="883ba-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="883ba-119">-CloudTiering</span></span>
<span data-ttu-id="883ba-120">클라우드 Tiering 매개 변수</span><span class="sxs-lookup"><span data-stu-id="883ba-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="883ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883ba-121">-DefaultProfile</span></span>
<span data-ttu-id="883ba-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883ba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="883ba-123">-InputObject</span></span>
<span data-ttu-id="883ba-124">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="883ba-125">-이름</span><span class="sxs-lookup"><span data-stu-id="883ba-125">-Name</span></span>
<span data-ttu-id="883ba-126">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="883ba-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="883ba-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="883ba-128">클라우드 시드 데이터 매개 변수</span><span class="sxs-lookup"><span data-stu-id="883ba-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="883ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="883ba-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="883ba-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="883ba-131">-ResourceId</span></span>
<span data-ttu-id="883ba-132">ServerEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="883ba-132">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="883ba-133">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="883ba-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="883ba-134">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="883ba-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="883ba-135">-SyncGroupName</span></span>
<span data-ttu-id="883ba-136">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-136">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="883ba-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="883ba-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="883ba-138">일 보다 오래 된 계층 파일 매개 변수</span><span class="sxs-lookup"><span data-stu-id="883ba-138">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="883ba-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="883ba-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="883ba-140">볼륨 사용 가능한 공간 백분율 매개 변수</span><span class="sxs-lookup"><span data-stu-id="883ba-140">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="883ba-141">-확인</span><span class="sxs-lookup"><span data-stu-id="883ba-141">-Confirm</span></span>
<span data-ttu-id="883ba-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883ba-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883ba-143">-WhatIf</span></span>
<span data-ttu-id="883ba-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="883ba-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883ba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883ba-146">CommonParameters</span></span>
<span data-ttu-id="883ba-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="883ba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883ba-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="883ba-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883ba-149">입력</span><span class="sxs-lookup"><span data-stu-id="883ba-149">INPUTS</span></span>

### <span data-ttu-id="883ba-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="883ba-150">System.String</span></span>

### <span data-ttu-id="883ba-151">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="883ba-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="883ba-152">출력</span><span class="sxs-lookup"><span data-stu-id="883ba-152">OUTPUTS</span></span>

### <span data-ttu-id="883ba-153">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="883ba-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="883ba-154">상속자</span><span class="sxs-lookup"><span data-stu-id="883ba-154">NOTES</span></span>

## <span data-ttu-id="883ba-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="883ba-155">RELATED LINKS</span></span>
