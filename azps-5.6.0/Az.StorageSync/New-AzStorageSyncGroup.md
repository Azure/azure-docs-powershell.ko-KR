---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011408"
---
# <span data-ttu-id="64ea9-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="64ea9-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="64ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="64ea9-103">이 명령은 지정된 저장소 동기화 서비스 내에서 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="64ea9-104">구문</span><span class="sxs-lookup"><span data-stu-id="64ea9-104">SYNTAX</span></span>

### <span data-ttu-id="64ea9-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="64ea9-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64ea9-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64ea9-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64ea9-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="64ea9-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64ea9-108">설명</span><span class="sxs-lookup"><span data-stu-id="64ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="64ea9-109">이 명령은 지정된 저장소 동기화 서비스 내에서 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="64ea9-110">동기화 그룹은 엔드포인트 중 하나에 저장된 모든 파일을 동기화하는 위치 토폴로지(엔드포인트라고도 하는 토폴로지)를 설명하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="64ea9-111">동기화 그룹에는 Azure 파일 공유를 참조하는 클라우드 엔드포인트가 포함되어 있으며, 등록된 서버에서 특정 로컬 경로를 참조하는 서버 엔드포인트도 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="64ea9-112">예제</span><span class="sxs-lookup"><span data-stu-id="64ea9-112">EXAMPLES</span></span>

### <span data-ttu-id="64ea9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="64ea9-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="64ea9-114">이 명령은 지정된 저장소 동기화 서비스 내에서 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="64ea9-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="64ea9-115">PARAMETERS</span></span>

### <span data-ttu-id="64ea9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ea9-116">-DefaultProfile</span></span>
<span data-ttu-id="64ea9-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ea9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="64ea9-118">-Name</span></span>
<span data-ttu-id="64ea9-119">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="64ea9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="64ea9-120">-ParentObject</span></span>
<span data-ttu-id="64ea9-121">StorageSyncService 개체는 일반적으로 매개 변수를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="64ea9-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="64ea9-122">-ParentResourceId</span></span>
<span data-ttu-id="64ea9-123">StorageSyncService 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="64ea9-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="64ea9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ea9-124">-ResourceGroupName</span></span>
<span data-ttu-id="64ea9-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="64ea9-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="64ea9-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="64ea9-127">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="64ea9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="64ea9-128">-Confirm</span></span>
<span data-ttu-id="64ea9-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64ea9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64ea9-130">-WhatIf</span></span>
<span data-ttu-id="64ea9-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64ea9-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64ea9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ea9-133">CommonParameters</span></span>
<span data-ttu-id="64ea9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64ea9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ea9-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="64ea9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ea9-136">입력</span><span class="sxs-lookup"><span data-stu-id="64ea9-136">INPUTS</span></span>

### <span data-ttu-id="64ea9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="64ea9-137">System.String</span></span>

### <span data-ttu-id="64ea9-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="64ea9-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="64ea9-139">출력</span><span class="sxs-lookup"><span data-stu-id="64ea9-139">OUTPUTS</span></span>

### <span data-ttu-id="64ea9-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="64ea9-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="64ea9-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64ea9-141">NOTES</span></span>

## <span data-ttu-id="64ea9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64ea9-142">RELATED LINKS</span></span>
