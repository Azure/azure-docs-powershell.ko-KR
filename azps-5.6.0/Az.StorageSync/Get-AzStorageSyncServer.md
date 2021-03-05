---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: 525d51d62477db88da78eaecc482d6cf64dbf810
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973152"
---
# <span data-ttu-id="b9dfe-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b9dfe-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="b9dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="b9dfe-103">이 명령은 주어진 저장소 동기화 서비스에 등록된 모든 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="b9dfe-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9dfe-104">SYNTAX</span></span>

### <span data-ttu-id="b9dfe-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9dfe-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9dfe-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9dfe-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9dfe-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9dfe-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9dfe-108">설명</span><span class="sxs-lookup"><span data-stu-id="b9dfe-108">DESCRIPTION</span></span>
<span data-ttu-id="b9dfe-109">이 명령은 주어진 저장소 동기화 서비스에 등록된 모든 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="b9dfe-110">또한 등록된 각 서버의 특성을 나열하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="b9dfe-111">예제</span><span class="sxs-lookup"><span data-stu-id="b9dfe-111">EXAMPLES</span></span>

### <span data-ttu-id="b9dfe-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9dfe-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b9dfe-113">이 명령은 특정 저장소 동기화 서비스에 등록된 모든 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="b9dfe-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9dfe-114">PARAMETERS</span></span>

### <span data-ttu-id="b9dfe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9dfe-115">-DefaultProfile</span></span>
<span data-ttu-id="b9dfe-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9dfe-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9dfe-117">-ParentObject</span></span>
<span data-ttu-id="b9dfe-118">StorageSyncService 개체는 일반적으로 매개 변수를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b9dfe-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9dfe-119">-ParentResourceId</span></span>
<span data-ttu-id="b9dfe-120">StorageSyncService 개체는 일반적으로 매개 변수를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b9dfe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9dfe-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9dfe-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9dfe-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b9dfe-123">-ServerId</span></span>
<span data-ttu-id="b9dfe-124">RegisteredServer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9dfe-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b9dfe-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="b9dfe-126">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b9dfe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9dfe-127">CommonParameters</span></span>
<span data-ttu-id="b9dfe-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9dfe-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9dfe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9dfe-130">입력</span><span class="sxs-lookup"><span data-stu-id="b9dfe-130">INPUTS</span></span>

### <span data-ttu-id="b9dfe-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b9dfe-131">System.String</span></span>

### <span data-ttu-id="b9dfe-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b9dfe-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="b9dfe-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b9dfe-133">System.Guid</span></span>

## <span data-ttu-id="b9dfe-134">출력</span><span class="sxs-lookup"><span data-stu-id="b9dfe-134">OUTPUTS</span></span>

### <span data-ttu-id="b9dfe-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b9dfe-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="b9dfe-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9dfe-136">NOTES</span></span>

## <span data-ttu-id="b9dfe-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9dfe-137">RELATED LINKS</span></span>
