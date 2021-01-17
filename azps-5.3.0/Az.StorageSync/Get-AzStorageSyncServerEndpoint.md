---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491220"
---
# <span data-ttu-id="b7151-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7151-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="b7151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7151-102">SYNOPSIS</span></span>
<span data-ttu-id="b7151-103">이 명령은 주어진 동기화 그룹 내의 모든 서버 엔드포인트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="b7151-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7151-104">SYNTAX</span></span>

### <span data-ttu-id="b7151-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7151-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7151-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7151-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7151-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7151-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7151-108">설명</span><span class="sxs-lookup"><span data-stu-id="b7151-108">DESCRIPTION</span></span>
<span data-ttu-id="b7151-109">이 명령은 주어진 동기화 그룹 내의 모든 서버 엔드포인트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="b7151-110">또한 각 서버 엔드포인트의 특성을 나열하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="b7151-111">예제</span><span class="sxs-lookup"><span data-stu-id="b7151-111">EXAMPLES</span></span>

### <span data-ttu-id="b7151-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7151-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="b7151-113">이 명령은 지정된 동기화 그룹 내에 포함된 모든 서버 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="b7151-114">특정 하나를 반환하도록 -ServerEndpointName을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="b7151-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7151-115">PARAMETERS</span></span>

### <span data-ttu-id="b7151-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7151-116">-DefaultProfile</span></span>
<span data-ttu-id="b7151-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7151-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b7151-118">-Name</span></span>
<span data-ttu-id="b7151-119">서버 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="b7151-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b7151-120">-ParentObject</span></span>
<span data-ttu-id="b7151-121">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b7151-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b7151-122">-ParentResourceId</span></span>
<span data-ttu-id="b7151-123">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b7151-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7151-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7151-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7151-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b7151-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="b7151-127">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b7151-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b7151-128">-SyncGroupName</span></span>
<span data-ttu-id="b7151-129">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="b7151-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7151-130">CommonParameters</span></span>
<span data-ttu-id="b7151-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7151-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7151-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7151-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7151-133">입력</span><span class="sxs-lookup"><span data-stu-id="b7151-133">INPUTS</span></span>

### <span data-ttu-id="b7151-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b7151-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="b7151-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b7151-135">System.String</span></span>

## <span data-ttu-id="b7151-136">출력</span><span class="sxs-lookup"><span data-stu-id="b7151-136">OUTPUTS</span></span>

### <span data-ttu-id="b7151-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7151-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="b7151-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7151-138">NOTES</span></span>

## <span data-ttu-id="b7151-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7151-139">RELATED LINKS</span></span>
