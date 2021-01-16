---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366633"
---
# <span data-ttu-id="c6beb-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c6beb-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="c6beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c6beb-103">이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="c6beb-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6beb-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6beb-105">설명</span><span class="sxs-lookup"><span data-stu-id="c6beb-105">DESCRIPTION</span></span>
<span data-ttu-id="c6beb-106">저장소 동기화 서비스는 Azure 파일 동기화에 대한 최상위 리소스입니다. 이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="c6beb-107">조직에서 고유한 서버 그룹을 구분하는 데 반드시 필요한 저장소 동기화 서비스를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="c6beb-108">저장소 동기화 서비스는 동기화 그룹을 포함하며 서버를 등록하기 위한 대상으로도 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="c6beb-109">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="c6beb-110">서버가 동일한 파일 집합 동기화에 참여해야 하는 경우 동일한 저장소 동기화 서비스에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="c6beb-111">예제</span><span class="sxs-lookup"><span data-stu-id="c6beb-111">EXAMPLES</span></span>

### <span data-ttu-id="c6beb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6beb-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="c6beb-113">이 명령은 저장소 동기화 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="c6beb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6beb-114">PARAMETERS</span></span>

### <span data-ttu-id="c6beb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6beb-115">-DefaultProfile</span></span>
<span data-ttu-id="c6beb-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6beb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c6beb-117">-Location</span></span>
<span data-ttu-id="c6beb-118">저장소 동기화 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="c6beb-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="c6beb-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="c6beb-120">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="c6beb-120">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="c6beb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c6beb-121">-Name</span></span>
<span data-ttu-id="c6beb-122">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="c6beb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6beb-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6beb-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6beb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6beb-125">-Tag</span></span>
<span data-ttu-id="c6beb-126">저장소 동기화 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="c6beb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6beb-127">-Confirm</span></span>
<span data-ttu-id="c6beb-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6beb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6beb-129">-WhatIf</span></span>
<span data-ttu-id="c6beb-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c6beb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6beb-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6beb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6beb-132">CommonParameters</span></span>
<span data-ttu-id="c6beb-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6beb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6beb-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c6beb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6beb-135">입력</span><span class="sxs-lookup"><span data-stu-id="c6beb-135">INPUTS</span></span>

### <span data-ttu-id="c6beb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c6beb-136">System.String</span></span>

## <span data-ttu-id="c6beb-137">출력</span><span class="sxs-lookup"><span data-stu-id="c6beb-137">OUTPUTS</span></span>

### <span data-ttu-id="c6beb-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c6beb-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c6beb-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6beb-139">NOTES</span></span>

## <span data-ttu-id="c6beb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6beb-140">RELATED LINKS</span></span>
