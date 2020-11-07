---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698500"
---
# <span data-ttu-id="9c7ec-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c7ec-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="9c7ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7ec-103">이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="9c7ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c7ec-104">SYNTAX</span></span>

### <span data-ttu-id="9c7ec-105">ObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9c7ec-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c7ec-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c7ec-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c7ec-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c7ec-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c7ec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9c7ec-108">DESCRIPTION</span></span>
<span data-ttu-id="9c7ec-109">이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="9c7ec-110">또한 각 서버 끝점의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="9c7ec-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9c7ec-111">EXAMPLES</span></span>

### <span data-ttu-id="9c7ec-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c7ec-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="9c7ec-113">이 명령은 지정 된 동기화 그룹 내에 포함 된 모든 서버 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="9c7ec-114">-ServerEndpointName를 지정 하 여 특정 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="9c7ec-115">변수</span><span class="sxs-lookup"><span data-stu-id="9c7ec-115">PARAMETERS</span></span>

### <span data-ttu-id="9c7ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7ec-116">-DefaultProfile</span></span>
<span data-ttu-id="9c7ec-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c7ec-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9c7ec-118">-Name</span></span>
<span data-ttu-id="9c7ec-119">서버 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ec-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9c7ec-120">-ParentObject</span></span>
<span data-ttu-id="9c7ec-121">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9c7ec-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9c7ec-122">-ParentResourceId</span></span>
<span data-ttu-id="9c7ec-123">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9c7ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c7ec-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9c7ec-126">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="9c7ec-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="9c7ec-127">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9c7ec-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7ec-128">-SyncGroupName</span></span>
<span data-ttu-id="9c7ec-129">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7ec-130">CommonParameters</span></span>
<span data-ttu-id="9c7ec-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7ec-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7ec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7ec-133">입력</span><span class="sxs-lookup"><span data-stu-id="9c7ec-133">INPUTS</span></span>

### <span data-ttu-id="9c7ec-134">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="9c7ec-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="9c7ec-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c7ec-135">System.String</span></span>

## <span data-ttu-id="9c7ec-136">출력</span><span class="sxs-lookup"><span data-stu-id="9c7ec-136">OUTPUTS</span></span>

### <span data-ttu-id="9c7ec-137">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c7ec-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="9c7ec-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9c7ec-138">NOTES</span></span>

## <span data-ttu-id="9c7ec-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c7ec-139">RELATED LINKS</span></span>
