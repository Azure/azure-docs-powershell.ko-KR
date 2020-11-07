---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698488"
---
# <span data-ttu-id="b3154-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b3154-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="b3154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3154-102">SYNOPSIS</span></span>
<span data-ttu-id="b3154-103">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="b3154-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3154-104">SYNTAX</span></span>

### <span data-ttu-id="b3154-105">ObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3154-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3154-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3154-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3154-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3154-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3154-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b3154-108">DESCRIPTION</span></span>
<span data-ttu-id="b3154-109">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="b3154-110">동기화 그룹은 끝점 이라고 하는 위치의 토폴로지를 설명 하는 데 사용 되며, 종점 중 하나에 저장 된 모든 파일을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="b3154-111">동기화 그룹에는 Azure 파일 공유를 참조 하는 클라우드 끝점이 포함 되며, 등록 된 서버의 특정 로컬 경로를 참조 하는 서버 끝점만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="b3154-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b3154-112">EXAMPLES</span></span>

### <span data-ttu-id="b3154-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3154-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="b3154-114">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="b3154-115">변수</span><span class="sxs-lookup"><span data-stu-id="b3154-115">PARAMETERS</span></span>

### <span data-ttu-id="b3154-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3154-116">-DefaultProfile</span></span>
<span data-ttu-id="b3154-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3154-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b3154-118">-Name</span></span>
<span data-ttu-id="b3154-119">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="b3154-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b3154-120">-ParentObject</span></span>
<span data-ttu-id="b3154-121">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b3154-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b3154-122">-ParentResourceId</span></span>
<span data-ttu-id="b3154-123">Storages Cservice 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b3154-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="b3154-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3154-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3154-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3154-126">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="b3154-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="b3154-127">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b3154-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3154-128">CommonParameters</span></span>
<span data-ttu-id="b3154-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3154-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3154-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3154-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3154-131">입력</span><span class="sxs-lookup"><span data-stu-id="b3154-131">INPUTS</span></span>

### <span data-ttu-id="b3154-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b3154-132">System.String</span></span>

### <span data-ttu-id="b3154-133">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="b3154-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b3154-134">출력</span><span class="sxs-lookup"><span data-stu-id="b3154-134">OUTPUTS</span></span>

### <span data-ttu-id="b3154-135">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="b3154-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="b3154-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b3154-136">NOTES</span></span>

## <span data-ttu-id="b3154-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3154-137">RELATED LINKS</span></span>
