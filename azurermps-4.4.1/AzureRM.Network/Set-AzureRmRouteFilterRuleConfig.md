---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529255"
---
# <span data-ttu-id="9a2aa-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a2aa-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="9a2aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2aa-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="9a2aa-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a2aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a2aa-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a2aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a2aa-105">DESCRIPTION</span></span>
<span data-ttu-id="9a2aa-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="9a2aa-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9a2aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9a2aa-107">EXAMPLES</span></span>

### <span data-ttu-id="9a2aa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a2aa-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9a2aa-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="9a2aa-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9a2aa-110">변수</span><span class="sxs-lookup"><span data-stu-id="9a2aa-110">PARAMETERS</span></span>

### <span data-ttu-id="9a2aa-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9a2aa-111">-Access</span></span>
<span data-ttu-id="9a2aa-112">규칙의 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-112">The access type of the rule.</span></span>
<span data-ttu-id="9a2aa-113">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 거부 '</span><span class="sxs-lookup"><span data-stu-id="9a2aa-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a2aa-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="9a2aa-114">-CommunityList</span></span>
<span data-ttu-id="9a2aa-115">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="9a2aa-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="9a2aa-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9a2aa-116">-Force</span></span>
<span data-ttu-id="9a2aa-117">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="9a2aa-117">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a2aa-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9a2aa-118">-Name</span></span>
<span data-ttu-id="9a2aa-119">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-119">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a2aa-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a2aa-120">-RouteFilter</span></span>
<span data-ttu-id="9a2aa-121">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a2aa-121">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a2aa-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="9a2aa-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="9a2aa-123">규칙의 경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="9a2aa-124">사용할 수 있는 값은 다음과 같습니다. ' 커뮤니티 '</span><span class="sxs-lookup"><span data-stu-id="9a2aa-124">Possible values are: 'Community'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a2aa-125">-확인</span><span class="sxs-lookup"><span data-stu-id="9a2aa-125">-Confirm</span></span>
<span data-ttu-id="9a2aa-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a2aa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a2aa-127">-WhatIf</span></span>
<span data-ttu-id="9a2aa-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a2aa-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a2aa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a2aa-130">-DefaultProfile</span></span>
<span data-ttu-id="9a2aa-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a2aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2aa-132">CommonParameters</span></span>
<span data-ttu-id="9a2aa-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2aa-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a2aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2aa-135">입력</span><span class="sxs-lookup"><span data-stu-id="9a2aa-135">INPUTS</span></span>

### <span data-ttu-id="9a2aa-136">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9a2aa-137">출력</span><span class="sxs-lookup"><span data-stu-id="9a2aa-137">OUTPUTS</span></span>

### <span data-ttu-id="9a2aa-138">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9a2aa-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9a2aa-139">상속자</span><span class="sxs-lookup"><span data-stu-id="9a2aa-139">NOTES</span></span>

## <span data-ttu-id="9a2aa-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a2aa-140">RELATED LINKS</span></span>

