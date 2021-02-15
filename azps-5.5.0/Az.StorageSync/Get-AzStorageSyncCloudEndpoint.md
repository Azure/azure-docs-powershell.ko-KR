---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183121"
---
# <span data-ttu-id="085b2-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="085b2-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="085b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="085b2-102">SYNOPSIS</span></span>
<span data-ttu-id="085b2-103">이 명령은 주어진 동기화 그룹 내의 모든 클라우드 엔드포인트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="085b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="085b2-104">SYNTAX</span></span>

### <span data-ttu-id="085b2-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="085b2-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="085b2-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="085b2-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="085b2-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="085b2-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="085b2-108">설명</span><span class="sxs-lookup"><span data-stu-id="085b2-108">DESCRIPTION</span></span>
<span data-ttu-id="085b2-109">이 명령은 주어진 동기화 그룹 내의 모든 클라우드 엔드포인트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="085b2-110">또한 각 클라우드 엔드포인트의 특성을 나열하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="085b2-111">예제</span><span class="sxs-lookup"><span data-stu-id="085b2-111">EXAMPLES</span></span>

### <span data-ttu-id="085b2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="085b2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="085b2-113">이 명령은 지정된 동기화 그룹 내에 포함된 모든 클라우드 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="085b2-114">특정 값을 반환하도록 -CloudEndpointName을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="085b2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="085b2-115">PARAMETERS</span></span>

### <span data-ttu-id="085b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085b2-116">-DefaultProfile</span></span>
<span data-ttu-id="085b2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="085b2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="085b2-118">-Name</span></span>
<span data-ttu-id="085b2-119">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="085b2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="085b2-120">-ParentObject</span></span>
<span data-ttu-id="085b2-121">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="085b2-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="085b2-122">-ParentResourceId</span></span>
<span data-ttu-id="085b2-123">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="085b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="085b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="085b2-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="085b2-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="085b2-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="085b2-127">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="085b2-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="085b2-128">-SyncGroupName</span></span>
<span data-ttu-id="085b2-129">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="085b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085b2-130">CommonParameters</span></span>
<span data-ttu-id="085b2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="085b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085b2-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="085b2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085b2-133">입력</span><span class="sxs-lookup"><span data-stu-id="085b2-133">INPUTS</span></span>

### <span data-ttu-id="085b2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="085b2-134">System.String</span></span>

### <span data-ttu-id="085b2-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="085b2-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="085b2-136">출력</span><span class="sxs-lookup"><span data-stu-id="085b2-136">OUTPUTS</span></span>

### <span data-ttu-id="085b2-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="085b2-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="085b2-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="085b2-138">NOTES</span></span>

## <span data-ttu-id="085b2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="085b2-139">RELATED LINKS</span></span>
