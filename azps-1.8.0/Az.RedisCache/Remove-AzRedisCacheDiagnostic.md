---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 6fcb8c2079ad26cc98c151aa55af00e475568db5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699538"
---
# <span data-ttu-id="a4ef2-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a4ef2-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="a4ef2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ef2-103">Azure Redis Cache에 대 한 진단을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="a4ef2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4ef2-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ef2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a4ef2-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ef2-106">**AzRedisCacheDiagnostic** Cmdlet은 Azure Redis Cache에 대 한 진단을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="a4ef2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a4ef2-107">EXAMPLES</span></span>

### <span data-ttu-id="a4ef2-108">예제 1: 진단 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a4ef2-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="a4ef2-109">이 명령은 지정 된 Azure Redis Cache에 대 한 진단을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="a4ef2-110">이렇게 하면 구독에 대해 동일한 지역의 모든 Azure Redis 캐시에 대 한 진단이 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="a4ef2-111">변수</span><span class="sxs-lookup"><span data-stu-id="a4ef2-111">PARAMETERS</span></span>

### <span data-ttu-id="a4ef2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ef2-112">-DefaultProfile</span></span>
<span data-ttu-id="a4ef2-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4ef2-114">-이름</span><span class="sxs-lookup"><span data-stu-id="a4ef2-114">-Name</span></span>
<span data-ttu-id="a4ef2-115">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="a4ef2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ef2-116">-ResourceGroupName</span></span>
<span data-ttu-id="a4ef2-117">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="a4ef2-118">-확인</span><span class="sxs-lookup"><span data-stu-id="a4ef2-118">-Confirm</span></span>
<span data-ttu-id="a4ef2-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ef2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ef2-120">-WhatIf</span></span>
<span data-ttu-id="a4ef2-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ef2-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ef2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ef2-123">CommonParameters</span></span>
<span data-ttu-id="a4ef2-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4ef2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ef2-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ef2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ef2-126">입력</span><span class="sxs-lookup"><span data-stu-id="a4ef2-126">INPUTS</span></span>

### <span data-ttu-id="a4ef2-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a4ef2-127">System.String</span></span>

## <span data-ttu-id="a4ef2-128">출력</span><span class="sxs-lookup"><span data-stu-id="a4ef2-128">OUTPUTS</span></span>

### <span data-ttu-id="a4ef2-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a4ef2-129">System.Void</span></span>

## <span data-ttu-id="a4ef2-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a4ef2-130">NOTES</span></span>
* <span data-ttu-id="a4ef2-131">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="a4ef2-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a4ef2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4ef2-132">RELATED LINKS</span></span>

[<span data-ttu-id="a4ef2-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a4ef2-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


