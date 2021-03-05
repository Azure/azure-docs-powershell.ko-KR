---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: d32fe3286a8c6e4b723137f8b20921c79caa45be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985670"
---
# <span data-ttu-id="12755-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="12755-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="12755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12755-102">SYNOPSIS</span></span>
<span data-ttu-id="12755-103">Azure Redis Cache에서 진단을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12755-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="12755-104">구문</span><span class="sxs-lookup"><span data-stu-id="12755-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12755-105">설명</span><span class="sxs-lookup"><span data-stu-id="12755-105">DESCRIPTION</span></span>
<span data-ttu-id="12755-106">**Remove-AzRedisCacheDiagnostic** cmdlet은 Azure Redis Cache에서 진단을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12755-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="12755-107">예제</span><span class="sxs-lookup"><span data-stu-id="12755-107">EXAMPLES</span></span>

### <span data-ttu-id="12755-108">예제 1: 진단 사용 안 하여</span><span class="sxs-lookup"><span data-stu-id="12755-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="12755-109">이 명령은 지정된 Azure Redis Cache에서 진단을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12755-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="12755-110">이렇게 하여 구독에 대해 동일한 지역에 있는 모든 Azure Redis Caches에 대한 진단을 사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="12755-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="12755-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="12755-111">PARAMETERS</span></span>

### <span data-ttu-id="12755-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12755-112">-DefaultProfile</span></span>
<span data-ttu-id="12755-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12755-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12755-114">-Name</span><span class="sxs-lookup"><span data-stu-id="12755-114">-Name</span></span>
<span data-ttu-id="12755-115">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12755-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="12755-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12755-116">-ResourceGroupName</span></span>
<span data-ttu-id="12755-117">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12755-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="12755-118">-확인</span><span class="sxs-lookup"><span data-stu-id="12755-118">-Confirm</span></span>
<span data-ttu-id="12755-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12755-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12755-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12755-120">-WhatIf</span></span>
<span data-ttu-id="12755-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="12755-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12755-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12755-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12755-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12755-123">CommonParameters</span></span>
<span data-ttu-id="12755-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12755-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12755-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12755-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12755-126">입력</span><span class="sxs-lookup"><span data-stu-id="12755-126">INPUTS</span></span>

### <span data-ttu-id="12755-127">System.String</span><span class="sxs-lookup"><span data-stu-id="12755-127">System.String</span></span>

## <span data-ttu-id="12755-128">출력</span><span class="sxs-lookup"><span data-stu-id="12755-128">OUTPUTS</span></span>

### <span data-ttu-id="12755-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="12755-129">System.Void</span></span>

## <span data-ttu-id="12755-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12755-130">NOTES</span></span>
* <span data-ttu-id="12755-131">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="12755-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="12755-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12755-132">RELATED LINKS</span></span>

[<span data-ttu-id="12755-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="12755-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


