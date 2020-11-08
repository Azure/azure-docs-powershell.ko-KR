---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042449"
---
# <span data-ttu-id="5ca4f-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ca4f-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="5ca4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca4f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca4f-103">이 명령은 지정 된 동기화 그룹 내의 모든 클라우드 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="5ca4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ca4f-104">SYNTAX</span></span>

### <span data-ttu-id="5ca4f-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ca4f-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca4f-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ca4f-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca4f-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ca4f-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca4f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5ca4f-108">DESCRIPTION</span></span>
<span data-ttu-id="5ca4f-109">이 명령은 지정 된 동기화 그룹 내의 모든 클라우드 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="5ca4f-110">또한 각 클라우드 끝점의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="5ca4f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5ca4f-111">EXAMPLES</span></span>

### <span data-ttu-id="5ca4f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ca4f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="5ca4f-113">이 명령은 지정 된 동기화 그룹 내에 포함 된 모든 클라우드 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="5ca4f-114">-CloudEndpointName를 지정 하 여 특정 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="5ca4f-115">변수</span><span class="sxs-lookup"><span data-stu-id="5ca4f-115">PARAMETERS</span></span>

### <span data-ttu-id="5ca4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca4f-116">-DefaultProfile</span></span>
<span data-ttu-id="5ca4f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca4f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="5ca4f-118">-Name</span></span>
<span data-ttu-id="5ca4f-119">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca4f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ca4f-120">-ParentObject</span></span>
<span data-ttu-id="5ca4f-121">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5ca4f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca4f-122">-ParentResourceId</span></span>
<span data-ttu-id="5ca4f-123">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="5ca4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ca4f-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5ca4f-126">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="5ca4f-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="5ca4f-127">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5ca4f-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca4f-128">-SyncGroupName</span></span>
<span data-ttu-id="5ca4f-129">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="5ca4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca4f-130">CommonParameters</span></span>
<span data-ttu-id="5ca4f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca4f-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca4f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca4f-133">입력</span><span class="sxs-lookup"><span data-stu-id="5ca4f-133">INPUTS</span></span>

### <span data-ttu-id="5ca4f-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ca4f-134">System.String</span></span>

### <span data-ttu-id="5ca4f-135">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="5ca4f-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="5ca4f-136">출력</span><span class="sxs-lookup"><span data-stu-id="5ca4f-136">OUTPUTS</span></span>

### <span data-ttu-id="5ca4f-137">StorageSync. c c i. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ca4f-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="5ca4f-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5ca4f-138">NOTES</span></span>

## <span data-ttu-id="5ca4f-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ca4f-139">RELATED LINKS</span></span>
