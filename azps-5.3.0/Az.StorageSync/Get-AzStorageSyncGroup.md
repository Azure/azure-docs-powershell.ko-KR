---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491228"
---
# <span data-ttu-id="98836-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="98836-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="98836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98836-102">SYNOPSIS</span></span>
<span data-ttu-id="98836-103">이 명령은 주어진 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="98836-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="98836-104">구문</span><span class="sxs-lookup"><span data-stu-id="98836-104">SYNTAX</span></span>

### <span data-ttu-id="98836-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="98836-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98836-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98836-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98836-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="98836-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98836-108">설명</span><span class="sxs-lookup"><span data-stu-id="98836-108">DESCRIPTION</span></span>
<span data-ttu-id="98836-109">이 명령은 주어진 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="98836-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="98836-110">또한 각 동기화 그룹의 특성을 나열하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98836-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="98836-111">예제</span><span class="sxs-lookup"><span data-stu-id="98836-111">EXAMPLES</span></span>

### <span data-ttu-id="98836-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="98836-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="98836-113">이 명령은 지정된 저장소 동기화 서비스에 포함된 모든 동기화 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98836-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="98836-114">특정 이름을 반환하도록 -Name을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98836-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="98836-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98836-115">PARAMETERS</span></span>

### <span data-ttu-id="98836-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98836-116">-DefaultProfile</span></span>
<span data-ttu-id="98836-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98836-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98836-118">-Name</span><span class="sxs-lookup"><span data-stu-id="98836-118">-Name</span></span>
<span data-ttu-id="98836-119">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98836-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="98836-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="98836-120">-ParentObject</span></span>
<span data-ttu-id="98836-121">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="98836-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="98836-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="98836-122">-ParentResourceId</span></span>
<span data-ttu-id="98836-123">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="98836-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="98836-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98836-124">-ResourceGroupName</span></span>
<span data-ttu-id="98836-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98836-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="98836-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="98836-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="98836-127">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98836-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="98836-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98836-128">CommonParameters</span></span>
<span data-ttu-id="98836-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98836-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98836-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="98836-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98836-131">입력</span><span class="sxs-lookup"><span data-stu-id="98836-131">INPUTS</span></span>

### <span data-ttu-id="98836-132">System.String</span><span class="sxs-lookup"><span data-stu-id="98836-132">System.String</span></span>

### <span data-ttu-id="98836-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="98836-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="98836-134">출력</span><span class="sxs-lookup"><span data-stu-id="98836-134">OUTPUTS</span></span>

### <span data-ttu-id="98836-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="98836-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="98836-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98836-136">NOTES</span></span>

## <span data-ttu-id="98836-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98836-137">RELATED LINKS</span></span>
