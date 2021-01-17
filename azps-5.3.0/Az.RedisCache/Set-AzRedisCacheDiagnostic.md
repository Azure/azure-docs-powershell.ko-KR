---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490699"
---
# <span data-ttu-id="fd3d9-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fd3d9-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="fd3d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3d9-103">Azure Redis Cache에서 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="fd3d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd3d9-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd3d9-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd3d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fd3d9-106">**Set-AzRedisCacheDiagnostic** cmdlet을 사용하면 Azure Redis Cache에 대한 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="fd3d9-107">예제</span><span class="sxs-lookup"><span data-stu-id="fd3d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fd3d9-108">예제 1: 진단 사용</span><span class="sxs-lookup"><span data-stu-id="fd3d9-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="fd3d9-109">이 명령을 사용하면 Azure Redis Cache에 대한 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="fd3d9-110">이 명령은 구독에 대해 동일한 지역에 있는 모든 Azure Redis Cache에 대한 진단을 사용하도록 설정하거나 저장소 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="fd3d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd3d9-111">PARAMETERS</span></span>

### <span data-ttu-id="fd3d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3d9-112">-DefaultProfile</span></span>
<span data-ttu-id="fd3d9-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd3d9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="fd3d9-114">-Name</span></span>
<span data-ttu-id="fd3d9-115">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-115">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3d9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3d9-116">-ResourceGroupName</span></span>
<span data-ttu-id="fd3d9-117">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3d9-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fd3d9-118">-StorageAccountId</span></span>
<span data-ttu-id="fd3d9-119">진단 데이터를 저장하는 데 사용되는 저장소 계정의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3d9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd3d9-120">-Confirm</span></span>
<span data-ttu-id="fd3d9-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3d9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3d9-122">-WhatIf</span></span>
<span data-ttu-id="fd3d9-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fd3d9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd3d9-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3d9-125">CommonParameters</span></span>
<span data-ttu-id="fd3d9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3d9-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3d9-128">입력</span><span class="sxs-lookup"><span data-stu-id="fd3d9-128">INPUTS</span></span>

### <span data-ttu-id="fd3d9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fd3d9-129">System.String</span></span>

## <span data-ttu-id="fd3d9-130">출력</span><span class="sxs-lookup"><span data-stu-id="fd3d9-130">OUTPUTS</span></span>

### <span data-ttu-id="fd3d9-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="fd3d9-131">System.Void</span></span>

## <span data-ttu-id="fd3d9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd3d9-132">NOTES</span></span>
* <span data-ttu-id="fd3d9-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="fd3d9-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="fd3d9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd3d9-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd3d9-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fd3d9-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


