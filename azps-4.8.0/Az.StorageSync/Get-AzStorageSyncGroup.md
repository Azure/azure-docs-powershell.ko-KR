---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204207"
---
# <span data-ttu-id="0fcc4-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0fcc4-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="0fcc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fcc4-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcc4-103">이 명령은 지정 된 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="0fcc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fcc4-104">SYNTAX</span></span>

### <span data-ttu-id="0fcc4-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0fcc4-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fcc4-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fcc4-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fcc4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fcc4-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fcc4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0fcc4-108">DESCRIPTION</span></span>
<span data-ttu-id="0fcc4-109">이 명령은 지정 된 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="0fcc4-110">또한 각 동기화 그룹의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="0fcc4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0fcc4-111">EXAMPLES</span></span>

### <span data-ttu-id="0fcc4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0fcc4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="0fcc4-113">이 명령은 지정 된 저장소 동기화 서비스 내에 포함 된 모든 동기화 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="0fcc4-114">-Name을 지정 하 여 특정 이름을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="0fcc4-115">변수</span><span class="sxs-lookup"><span data-stu-id="0fcc4-115">PARAMETERS</span></span>

### <span data-ttu-id="0fcc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fcc4-116">-DefaultProfile</span></span>
<span data-ttu-id="0fcc4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fcc4-118">-이름</span><span class="sxs-lookup"><span data-stu-id="0fcc4-118">-Name</span></span>
<span data-ttu-id="0fcc4-119">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fcc4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0fcc4-120">-ParentObject</span></span>
<span data-ttu-id="0fcc4-121">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0fcc4-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0fcc4-122">-ParentResourceId</span></span>
<span data-ttu-id="0fcc4-123">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0fcc4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fcc4-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fcc4-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0fcc4-126">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="0fcc4-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="0fcc4-127">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0fcc4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcc4-128">CommonParameters</span></span>
<span data-ttu-id="0fcc4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcc4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcc4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fcc4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcc4-131">입력</span><span class="sxs-lookup"><span data-stu-id="0fcc4-131">INPUTS</span></span>

### <span data-ttu-id="0fcc4-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0fcc4-132">System.String</span></span>

### <span data-ttu-id="0fcc4-133">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="0fcc4-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="0fcc4-134">출력</span><span class="sxs-lookup"><span data-stu-id="0fcc4-134">OUTPUTS</span></span>

### <span data-ttu-id="0fcc4-135">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="0fcc4-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="0fcc4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0fcc4-136">NOTES</span></span>

## <span data-ttu-id="0fcc4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fcc4-137">RELATED LINKS</span></span>
