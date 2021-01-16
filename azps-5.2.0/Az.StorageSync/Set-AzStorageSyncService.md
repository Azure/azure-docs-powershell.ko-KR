---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366521"
---
# <span data-ttu-id="5667f-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5667f-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="5667f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5667f-102">SYNOPSIS</span></span>
<span data-ttu-id="5667f-103">이 명령은 리소스 그룹의 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="5667f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5667f-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5667f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5667f-105">DESCRIPTION</span></span>
<span data-ttu-id="5667f-106">저장소 동기화 서비스는 Azure 파일 동기화에 대한 최상위 리소스입니다. 이 명령은 리소스 그룹의 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="5667f-107">조직에서 고유한 서버 그룹을 구분하는 데 반드시 필요한 저장소 동기화 서비스를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="5667f-108">저장소 동기화 서비스는 동기화 그룹을 포함하며 서버를 등록하기 위한 대상으로도 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="5667f-109">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="5667f-110">서버가 동일한 파일 집합 동기화에 참여해야 하는 경우 동일한 저장소 동기화 서비스에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="5667f-111">예제</span><span class="sxs-lookup"><span data-stu-id="5667f-111">EXAMPLES</span></span>

### <span data-ttu-id="5667f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5667f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="5667f-113">이 명령은 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="5667f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5667f-114">PARAMETERS</span></span>

### <span data-ttu-id="5667f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5667f-115">-DefaultProfile</span></span>
<span data-ttu-id="5667f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="5667f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5667f-117">-Name</span></span>
<span data-ttu-id="5667f-118">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="5667f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5667f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5667f-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="5667f-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="5667f-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="5667f-122">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="5667f-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="5667f-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="5667f-123">-Tag</span></span>
<span data-ttu-id="5667f-124">저장소 동기화 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="5667f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5667f-125">-Confirm</span></span>
<span data-ttu-id="5667f-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5667f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5667f-127">-WhatIf</span></span>
<span data-ttu-id="5667f-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5667f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5667f-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5667f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5667f-130">CommonParameters</span></span>
<span data-ttu-id="5667f-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5667f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5667f-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5667f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5667f-133">입력</span><span class="sxs-lookup"><span data-stu-id="5667f-133">INPUTS</span></span>

### <span data-ttu-id="5667f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5667f-134">System.String</span></span>

## <span data-ttu-id="5667f-135">출력</span><span class="sxs-lookup"><span data-stu-id="5667f-135">OUTPUTS</span></span>

### <span data-ttu-id="5667f-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5667f-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="5667f-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5667f-137">NOTES</span></span>

## <span data-ttu-id="5667f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5667f-138">RELATED LINKS</span></span>
