---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: c24bf60171e152985fb13204f23082f94f8c7ff0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011360"
---
# <span data-ttu-id="fd939-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fd939-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="fd939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd939-102">SYNOPSIS</span></span>
<span data-ttu-id="fd939-103">이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="fd939-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd939-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd939-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd939-105">DESCRIPTION</span></span>
<span data-ttu-id="fd939-106">저장소 동기화 서비스는 Azure 파일 동기화의 최상위 리소스입니다. 이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="fd939-107">조직에서 고유한 서버 그룹을 구분하는 데 반드시 필요한 저장소 동기화 서비스를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="fd939-108">저장소 동기화 서비스는 동기화 그룹을 포함하며 서버를 등록하는 대상으로도 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="fd939-109">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="fd939-110">서버가 동일한 파일 집합을 동기화하는 데 참여해야 하는 경우 동일한 저장소 동기화 서비스에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="fd939-111">예제</span><span class="sxs-lookup"><span data-stu-id="fd939-111">EXAMPLES</span></span>

### <span data-ttu-id="fd939-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd939-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="fd939-113">이 명령은 저장소 동기화 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="fd939-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fd939-114">PARAMETERS</span></span>

### <span data-ttu-id="fd939-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd939-115">-DefaultProfile</span></span>
<span data-ttu-id="fd939-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd939-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fd939-117">-Location</span></span>
<span data-ttu-id="fd939-118">저장소 동기화 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd939-119">-들어오는TrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="fd939-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="fd939-120">Storage Sync Service 들어오는TrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="fd939-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd939-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fd939-121">-Name</span></span>
<span data-ttu-id="fd939-122">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-122">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd939-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd939-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd939-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd939-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd939-125">-Tag</span></span>
<span data-ttu-id="fd939-126">Storage 동기화 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-126">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd939-127">-확인</span><span class="sxs-lookup"><span data-stu-id="fd939-127">-Confirm</span></span>
<span data-ttu-id="fd939-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd939-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd939-129">-WhatIf</span></span>
<span data-ttu-id="fd939-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd939-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd939-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd939-132">CommonParameters</span></span>
<span data-ttu-id="fd939-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd939-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd939-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fd939-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd939-135">입력</span><span class="sxs-lookup"><span data-stu-id="fd939-135">INPUTS</span></span>

### <span data-ttu-id="fd939-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fd939-136">System.String</span></span>

## <span data-ttu-id="fd939-137">출력</span><span class="sxs-lookup"><span data-stu-id="fd939-137">OUTPUTS</span></span>

### <span data-ttu-id="fd939-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fd939-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="fd939-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd939-139">NOTES</span></span>

## <span data-ttu-id="fd939-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd939-140">RELATED LINKS</span></span>
