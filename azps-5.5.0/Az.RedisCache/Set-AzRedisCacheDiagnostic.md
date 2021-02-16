---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186553"
---
# <span data-ttu-id="1dcb0-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1dcb0-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="1dcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcb0-103">Azure Redis Cache에서 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="1dcb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dcb0-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dcb0-105">설명</span><span class="sxs-lookup"><span data-stu-id="1dcb0-105">DESCRIPTION</span></span>
<span data-ttu-id="1dcb0-106">**Set-AzRedisCacheDiagnostic** cmdlet을 사용하면 Azure Redis Cache에 대한 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="1dcb0-107">예제</span><span class="sxs-lookup"><span data-stu-id="1dcb0-107">EXAMPLES</span></span>

### <span data-ttu-id="1dcb0-108">예제 1: 진단 사용</span><span class="sxs-lookup"><span data-stu-id="1dcb0-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="1dcb0-109">이 명령을 사용하면 Azure Redis Cache에 대한 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="1dcb0-110">이 명령은 구독에 대해 동일한 지역에 있는 모든 Azure Redis Cache에 대한 진단을 사용하도록 설정하거나 저장소 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="1dcb0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dcb0-111">PARAMETERS</span></span>

### <span data-ttu-id="1dcb0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcb0-112">-DefaultProfile</span></span>
<span data-ttu-id="1dcb0-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dcb0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1dcb0-114">-Name</span></span>
<span data-ttu-id="1dcb0-115">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="1dcb0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dcb0-116">-ResourceGroupName</span></span>
<span data-ttu-id="1dcb0-117">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="1dcb0-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1dcb0-118">-StorageAccountId</span></span>
<span data-ttu-id="1dcb0-119">진단 데이터를 저장하는 데 사용되는 저장소 계정의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="1dcb0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dcb0-120">-Confirm</span></span>
<span data-ttu-id="1dcb0-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dcb0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dcb0-122">-WhatIf</span></span>
<span data-ttu-id="1dcb0-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1dcb0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dcb0-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dcb0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcb0-125">CommonParameters</span></span>
<span data-ttu-id="1dcb0-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcb0-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcb0-128">입력</span><span class="sxs-lookup"><span data-stu-id="1dcb0-128">INPUTS</span></span>

### <span data-ttu-id="1dcb0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1dcb0-129">System.String</span></span>

## <span data-ttu-id="1dcb0-130">출력</span><span class="sxs-lookup"><span data-stu-id="1dcb0-130">OUTPUTS</span></span>

### <span data-ttu-id="1dcb0-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="1dcb0-131">System.Void</span></span>

## <span data-ttu-id="1dcb0-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dcb0-132">NOTES</span></span>
* <span data-ttu-id="1dcb0-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="1dcb0-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1dcb0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dcb0-134">RELATED LINKS</span></span>

[<span data-ttu-id="1dcb0-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1dcb0-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


