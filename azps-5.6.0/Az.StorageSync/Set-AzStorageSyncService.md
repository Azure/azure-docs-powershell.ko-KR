---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: f7b3f0924b1033f1c3b4ffd773ebbbbed985fa3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973995"
---
# <span data-ttu-id="3cc06-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3cc06-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="3cc06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc06-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc06-103">이 명령은 리소스 그룹의 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="3cc06-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cc06-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc06-105">설명</span><span class="sxs-lookup"><span data-stu-id="3cc06-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc06-106">저장소 동기화 서비스는 Azure 파일 동기화의 최상위 리소스입니다. 이 명령은 리소스 그룹의 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="3cc06-107">조직에서 고유한 서버 그룹을 구분하는 데 반드시 필요한 저장소 동기화 서비스를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="3cc06-108">저장소 동기화 서비스는 동기화 그룹을 포함하며 서버를 등록하는 대상으로도 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="3cc06-109">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="3cc06-110">서버가 동일한 파일 집합을 동기화하는 데 참여해야 하는 경우 동일한 저장소 동기화 서비스에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="3cc06-111">예제</span><span class="sxs-lookup"><span data-stu-id="3cc06-111">EXAMPLES</span></span>

### <span data-ttu-id="3cc06-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cc06-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="3cc06-113">이 명령은 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="3cc06-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3cc06-114">PARAMETERS</span></span>

### <span data-ttu-id="3cc06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc06-115">-DefaultProfile</span></span>
<span data-ttu-id="3cc06-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="3cc06-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3cc06-117">-Name</span></span>
<span data-ttu-id="3cc06-118">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="3cc06-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc06-119">-ResourceGroupName</span></span>
<span data-ttu-id="3cc06-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="3cc06-121">-들어오는TrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc06-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="3cc06-122">Storage Sync Service 들어오는TrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc06-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="3cc06-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cc06-123">-Tag</span></span>
<span data-ttu-id="3cc06-124">Storage 동기화 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="3cc06-125">-확인</span><span class="sxs-lookup"><span data-stu-id="3cc06-125">-Confirm</span></span>
<span data-ttu-id="3cc06-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc06-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc06-127">-WhatIf</span></span>
<span data-ttu-id="3cc06-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cc06-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc06-130">CommonParameters</span></span>
<span data-ttu-id="3cc06-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc06-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3cc06-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc06-133">입력</span><span class="sxs-lookup"><span data-stu-id="3cc06-133">INPUTS</span></span>

### <span data-ttu-id="3cc06-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3cc06-134">System.String</span></span>

## <span data-ttu-id="3cc06-135">출력</span><span class="sxs-lookup"><span data-stu-id="3cc06-135">OUTPUTS</span></span>

### <span data-ttu-id="3cc06-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3cc06-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="3cc06-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cc06-137">NOTES</span></span>

## <span data-ttu-id="3cc06-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cc06-138">RELATED LINKS</span></span>
