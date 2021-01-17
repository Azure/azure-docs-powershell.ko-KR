---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491204"
---
# <span data-ttu-id="312b7-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="312b7-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="312b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="312b7-102">SYNOPSIS</span></span>
<span data-ttu-id="312b7-103">이 명령은 지정된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="312b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="312b7-104">SYNTAX</span></span>

### <span data-ttu-id="312b7-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="312b7-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="312b7-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="312b7-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="312b7-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="312b7-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="312b7-108">설명</span><span class="sxs-lookup"><span data-stu-id="312b7-108">DESCRIPTION</span></span>
<span data-ttu-id="312b7-109">이 명령은 지정된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="312b7-110">동기화 그룹은 엔드포인트 중 하나에 저장된 모든 파일을 동기화하는 위치의 토폴로지(엔드포인트라고도 하는)를 설명하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="312b7-111">동기화 그룹에는 Azure 파일 공유를 참조하는 클라우드 엔드포인트가 포함되어 있으며 등록된 서버에서 특정 로컬 경로를 참조하는 서버 엔드포인트도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="312b7-112">예제</span><span class="sxs-lookup"><span data-stu-id="312b7-112">EXAMPLES</span></span>

### <span data-ttu-id="312b7-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="312b7-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="312b7-114">이 명령은 지정된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="312b7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="312b7-115">PARAMETERS</span></span>

### <span data-ttu-id="312b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312b7-116">-DefaultProfile</span></span>
<span data-ttu-id="312b7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="312b7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="312b7-118">-Name</span></span>
<span data-ttu-id="312b7-119">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312b7-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="312b7-120">-ParentObject</span></span>
<span data-ttu-id="312b7-121">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="312b7-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="312b7-122">-ParentResourceId</span></span>
<span data-ttu-id="312b7-123">StorageSyncService 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="312b7-123">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="312b7-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312b7-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="312b7-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="312b7-127">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312b7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="312b7-128">-Confirm</span></span>
<span data-ttu-id="312b7-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="312b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="312b7-130">-WhatIf</span></span>
<span data-ttu-id="312b7-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="312b7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="312b7-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="312b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312b7-133">CommonParameters</span></span>
<span data-ttu-id="312b7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="312b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312b7-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="312b7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312b7-136">입력</span><span class="sxs-lookup"><span data-stu-id="312b7-136">INPUTS</span></span>

### <span data-ttu-id="312b7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="312b7-137">System.String</span></span>

### <span data-ttu-id="312b7-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="312b7-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="312b7-139">출력</span><span class="sxs-lookup"><span data-stu-id="312b7-139">OUTPUTS</span></span>

### <span data-ttu-id="312b7-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="312b7-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="312b7-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="312b7-141">NOTES</span></span>

## <span data-ttu-id="312b7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="312b7-142">RELATED LINKS</span></span>
