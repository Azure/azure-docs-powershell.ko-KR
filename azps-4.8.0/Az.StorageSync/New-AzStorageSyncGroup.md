---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213782"
---
# <span data-ttu-id="b18fa-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b18fa-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="b18fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b18fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b18fa-103">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="b18fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b18fa-104">SYNTAX</span></span>

### <span data-ttu-id="b18fa-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b18fa-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b18fa-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b18fa-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b18fa-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b18fa-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b18fa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b18fa-108">DESCRIPTION</span></span>
<span data-ttu-id="b18fa-109">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="b18fa-110">동기화 그룹은 끝점 이라고 하는 위치의 토폴로지를 설명 하는 데 사용 되며, 종점 중 하나에 저장 된 모든 파일을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="b18fa-111">동기화 그룹에는 Azure 파일 공유를 참조 하는 클라우드 끝점이 포함 되며, 등록 된 서버의 특정 로컬 경로를 참조 하는 서버 끝점만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="b18fa-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b18fa-112">EXAMPLES</span></span>

### <span data-ttu-id="b18fa-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b18fa-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="b18fa-114">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="b18fa-115">변수</span><span class="sxs-lookup"><span data-stu-id="b18fa-115">PARAMETERS</span></span>

### <span data-ttu-id="b18fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18fa-116">-DefaultProfile</span></span>
<span data-ttu-id="b18fa-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b18fa-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b18fa-118">-Name</span></span>
<span data-ttu-id="b18fa-119">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="b18fa-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b18fa-120">-ParentObject</span></span>
<span data-ttu-id="b18fa-121">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b18fa-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b18fa-122">-ParentResourceId</span></span>
<span data-ttu-id="b18fa-123">Storages Cservice 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b18fa-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="b18fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b18fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="b18fa-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b18fa-126">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="b18fa-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="b18fa-127">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b18fa-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b18fa-128">-Confirm</span></span>
<span data-ttu-id="b18fa-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b18fa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b18fa-130">-WhatIf</span></span>
<span data-ttu-id="b18fa-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b18fa-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b18fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18fa-133">CommonParameters</span></span>
<span data-ttu-id="b18fa-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18fa-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b18fa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18fa-136">입력</span><span class="sxs-lookup"><span data-stu-id="b18fa-136">INPUTS</span></span>

### <span data-ttu-id="b18fa-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b18fa-137">System.String</span></span>

### <span data-ttu-id="b18fa-138">StorageSync. Psstorages<c13> Cservice</span><span class="sxs-lookup"><span data-stu-id="b18fa-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b18fa-139">출력</span><span class="sxs-lookup"><span data-stu-id="b18fa-139">OUTPUTS</span></span>

### <span data-ttu-id="b18fa-140">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="b18fa-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="b18fa-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b18fa-141">NOTES</span></span>

## <span data-ttu-id="b18fa-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b18fa-142">RELATED LINKS</span></span>
