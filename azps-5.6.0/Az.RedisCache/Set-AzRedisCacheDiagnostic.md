---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: ee6e2848325222d86271bfd70705ec7aa855cbb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000891"
---
# <span data-ttu-id="efd56-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="efd56-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="efd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd56-102">SYNOPSIS</span></span>
<span data-ttu-id="efd56-103">Azure Redis Cache에서 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="efd56-104">구문</span><span class="sxs-lookup"><span data-stu-id="efd56-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd56-105">설명</span><span class="sxs-lookup"><span data-stu-id="efd56-105">DESCRIPTION</span></span>
<span data-ttu-id="efd56-106">**Set-AzRedisCacheDiagnostic** cmdlet을 사용하면 Azure Redis Cache에 대한 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="efd56-107">예제</span><span class="sxs-lookup"><span data-stu-id="efd56-107">EXAMPLES</span></span>

### <span data-ttu-id="efd56-108">예제 1: 진단 사용</span><span class="sxs-lookup"><span data-stu-id="efd56-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="efd56-109">이 명령을 사용하면 Azure Redis 캐시에 대한 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="efd56-110">이 명령은 진단을 사용하도록 설정하거나 구독에 대해 동일한 지역에 있는 모든 Azure Redis Caches에 대한 저장소 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="efd56-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="efd56-111">PARAMETERS</span></span>

### <span data-ttu-id="efd56-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd56-112">-DefaultProfile</span></span>
<span data-ttu-id="efd56-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efd56-114">-Name</span><span class="sxs-lookup"><span data-stu-id="efd56-114">-Name</span></span>
<span data-ttu-id="efd56-115">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="efd56-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd56-116">-ResourceGroupName</span></span>
<span data-ttu-id="efd56-117">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="efd56-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="efd56-118">-StorageAccountId</span></span>
<span data-ttu-id="efd56-119">진단 데이터를 저장하는 데 사용되는 저장소 계정의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="efd56-120">-확인</span><span class="sxs-lookup"><span data-stu-id="efd56-120">-Confirm</span></span>
<span data-ttu-id="efd56-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd56-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd56-122">-WhatIf</span></span>
<span data-ttu-id="efd56-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efd56-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd56-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd56-125">CommonParameters</span></span>
<span data-ttu-id="efd56-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efd56-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd56-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="efd56-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd56-128">입력</span><span class="sxs-lookup"><span data-stu-id="efd56-128">INPUTS</span></span>

### <span data-ttu-id="efd56-129">System.String</span><span class="sxs-lookup"><span data-stu-id="efd56-129">System.String</span></span>

## <span data-ttu-id="efd56-130">출력</span><span class="sxs-lookup"><span data-stu-id="efd56-130">OUTPUTS</span></span>

### <span data-ttu-id="efd56-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="efd56-131">System.Void</span></span>

## <span data-ttu-id="efd56-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efd56-132">NOTES</span></span>
* <span data-ttu-id="efd56-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="efd56-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="efd56-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efd56-134">RELATED LINKS</span></span>

[<span data-ttu-id="efd56-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="efd56-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


