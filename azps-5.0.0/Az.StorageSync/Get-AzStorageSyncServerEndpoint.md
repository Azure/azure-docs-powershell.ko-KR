---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310508"
---
# <span data-ttu-id="8179c-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8179c-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="8179c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8179c-102">SYNOPSIS</span></span>
<span data-ttu-id="8179c-103">이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="8179c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8179c-104">SYNTAX</span></span>

### <span data-ttu-id="8179c-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8179c-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8179c-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8179c-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8179c-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8179c-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8179c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8179c-108">DESCRIPTION</span></span>
<span data-ttu-id="8179c-109">이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="8179c-110">또한 각 서버 끝점의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="8179c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8179c-111">EXAMPLES</span></span>

### <span data-ttu-id="8179c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8179c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="8179c-113">이 명령은 지정 된 동기화 그룹 내에 포함 된 모든 서버 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="8179c-114">-ServerEndpointName를 지정 하 여 특정 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="8179c-115">변수</span><span class="sxs-lookup"><span data-stu-id="8179c-115">PARAMETERS</span></span>

### <span data-ttu-id="8179c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8179c-116">-DefaultProfile</span></span>
<span data-ttu-id="8179c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8179c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="8179c-118">-Name</span></span>
<span data-ttu-id="8179c-119">서버 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="8179c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8179c-120">-ParentObject</span></span>
<span data-ttu-id="8179c-121">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="8179c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8179c-122">-ParentResourceId</span></span>
<span data-ttu-id="8179c-123">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="8179c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8179c-124">-ResourceGroupName</span></span>
<span data-ttu-id="8179c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8179c-126">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="8179c-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="8179c-127">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8179c-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8179c-128">-SyncGroupName</span></span>
<span data-ttu-id="8179c-129">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="8179c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8179c-130">CommonParameters</span></span>
<span data-ttu-id="8179c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8179c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8179c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8179c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8179c-133">입력</span><span class="sxs-lookup"><span data-stu-id="8179c-133">INPUTS</span></span>

### <span data-ttu-id="8179c-134">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="8179c-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="8179c-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8179c-135">System.String</span></span>

## <span data-ttu-id="8179c-136">출력</span><span class="sxs-lookup"><span data-stu-id="8179c-136">OUTPUTS</span></span>

### <span data-ttu-id="8179c-137">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8179c-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="8179c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="8179c-138">NOTES</span></span>

## <span data-ttu-id="8179c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8179c-139">RELATED LINKS</span></span>
