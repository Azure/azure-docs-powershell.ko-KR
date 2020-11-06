---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 0725b75c15fa6ab977d0b829a1928943bfd9ed31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535268"
---
# <span data-ttu-id="682a7-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="682a7-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="682a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="682a7-102">SYNOPSIS</span></span>
<span data-ttu-id="682a7-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="682a7-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="682a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="682a7-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="682a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="682a7-105">DESCRIPTION</span></span>
<span data-ttu-id="682a7-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="682a7-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="682a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="682a7-107">EXAMPLES</span></span>

### <span data-ttu-id="682a7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="682a7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="682a7-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="682a7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="682a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="682a7-110">PARAMETERS</span></span>

### <span data-ttu-id="682a7-111">-Access</span><span class="sxs-lookup"><span data-stu-id="682a7-111">-Access</span></span>
<span data-ttu-id="682a7-112">규칙의 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-112">The access type of the rule.</span></span>
<span data-ttu-id="682a7-113">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 거부 '</span><span class="sxs-lookup"><span data-stu-id="682a7-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="682a7-114">-CommunityList</span></span>
<span data-ttu-id="682a7-115">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="682a7-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682a7-116">-DefaultProfile</span></span>
<span data-ttu-id="682a7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="682a7-118">-Force</span></span>
<span data-ttu-id="682a7-119">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="682a7-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-120">-이름</span><span class="sxs-lookup"><span data-stu-id="682a7-120">-Name</span></span>
<span data-ttu-id="682a7-121">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-121">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="682a7-122">-RouteFilter</span></span>
<span data-ttu-id="682a7-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="682a7-123">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="682a7-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="682a7-125">규칙의 경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="682a7-126">사용할 수 있는 값은 다음과 같습니다. ' 커뮤니티 '</span><span class="sxs-lookup"><span data-stu-id="682a7-126">Possible values are: 'Community'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-127">-확인</span><span class="sxs-lookup"><span data-stu-id="682a7-127">-Confirm</span></span>
<span data-ttu-id="682a7-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="682a7-129">-WhatIf</span></span>
<span data-ttu-id="682a7-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="682a7-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682a7-132">CommonParameters</span></span>
<span data-ttu-id="682a7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="682a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682a7-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="682a7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682a7-135">입력</span><span class="sxs-lookup"><span data-stu-id="682a7-135">INPUTS</span></span>

### <span data-ttu-id="682a7-136">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="682a7-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="682a7-137">출력</span><span class="sxs-lookup"><span data-stu-id="682a7-137">OUTPUTS</span></span>

### <span data-ttu-id="682a7-138">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="682a7-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="682a7-139">상속자</span><span class="sxs-lookup"><span data-stu-id="682a7-139">NOTES</span></span>

## <span data-ttu-id="682a7-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="682a7-140">RELATED LINKS</span></span>

