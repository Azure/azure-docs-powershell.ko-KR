---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: ea99137cdd97963bd3d16c9bf0d9b81012e3352b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535648"
---
# <span data-ttu-id="13c8f-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="13c8f-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="13c8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="13c8f-103">Azure Redis Cache에 대 한 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13c8f-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13c8f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="13c8f-106">AzureRmRedisCacheDiagnostics cmdlet은 Azure Redis Cache에 대 한 진단을 사용 하도록 **설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="13c8f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="13c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="13c8f-108">예제 1: 진단 사용</span><span class="sxs-lookup"><span data-stu-id="13c8f-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="13c8f-109">이 명령은 Azure Redis cache에 대 한 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="13c8f-110">이 명령은 구독에 대해 동일한 지역에서 모든 Azure Redis 캐시에 대 한 진단 또는 저장소 계정을 업데이트 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="13c8f-111">변수</span><span class="sxs-lookup"><span data-stu-id="13c8f-111">PARAMETERS</span></span>

### <span data-ttu-id="13c8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c8f-112">-DefaultProfile</span></span>
<span data-ttu-id="13c8f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c8f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="13c8f-114">-Name</span></span>
<span data-ttu-id="13c8f-115">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="13c8f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c8f-116">-ResourceGroupName</span></span>
<span data-ttu-id="13c8f-117">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="13c8f-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="13c8f-118">-StorageAccountId</span></span>
<span data-ttu-id="13c8f-119">진단 데이터를 저장 하는 데 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="13c8f-120">-확인</span><span class="sxs-lookup"><span data-stu-id="13c8f-120">-Confirm</span></span>
<span data-ttu-id="13c8f-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13c8f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c8f-122">-WhatIf</span></span>
<span data-ttu-id="13c8f-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13c8f-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13c8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c8f-125">CommonParameters</span></span>
<span data-ttu-id="13c8f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13c8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c8f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c8f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c8f-128">입력</span><span class="sxs-lookup"><span data-stu-id="13c8f-128">INPUTS</span></span>

### <span data-ttu-id="13c8f-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13c8f-129">System.String</span></span>

## <span data-ttu-id="13c8f-130">출력</span><span class="sxs-lookup"><span data-stu-id="13c8f-130">OUTPUTS</span></span>

### <span data-ttu-id="13c8f-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="13c8f-131">System.Void</span></span>

## <span data-ttu-id="13c8f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="13c8f-132">NOTES</span></span>
* <span data-ttu-id="13c8f-133">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="13c8f-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="13c8f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13c8f-134">RELATED LINKS</span></span>

[<span data-ttu-id="13c8f-135">제거-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="13c8f-135">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


