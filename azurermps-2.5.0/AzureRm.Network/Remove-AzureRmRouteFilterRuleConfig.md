---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881790"
---
# <span data-ttu-id="bf49b-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf49b-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bf49b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf49b-102">SYNOPSIS</span></span>
<span data-ttu-id="bf49b-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="bf49b-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf49b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf49b-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf49b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf49b-105">DESCRIPTION</span></span>
<span data-ttu-id="bf49b-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="bf49b-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="bf49b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf49b-107">EXAMPLES</span></span>

### <span data-ttu-id="bf49b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf49b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bf49b-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="bf49b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bf49b-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf49b-110">PARAMETERS</span></span>

### <span data-ttu-id="bf49b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf49b-111">-DefaultProfile</span></span>
<span data-ttu-id="bf49b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf49b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf49b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bf49b-113">-Force</span></span>
<span data-ttu-id="bf49b-114">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="bf49b-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="bf49b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="bf49b-115">-Name</span></span>
<span data-ttu-id="bf49b-116">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf49b-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="bf49b-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bf49b-117">-RouteFilter</span></span>
<span data-ttu-id="bf49b-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bf49b-118">The RouteFilter</span></span>

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

### <span data-ttu-id="bf49b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bf49b-119">-Confirm</span></span>
<span data-ttu-id="bf49b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf49b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf49b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf49b-121">-WhatIf</span></span>
<span data-ttu-id="bf49b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf49b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf49b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf49b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf49b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf49b-124">CommonParameters</span></span>
<span data-ttu-id="bf49b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf49b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf49b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf49b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf49b-127">입력</span><span class="sxs-lookup"><span data-stu-id="bf49b-127">INPUTS</span></span>

### <span data-ttu-id="bf49b-128">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bf49b-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bf49b-129">출력</span><span class="sxs-lookup"><span data-stu-id="bf49b-129">OUTPUTS</span></span>

### <span data-ttu-id="bf49b-130">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bf49b-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="bf49b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bf49b-131">NOTES</span></span>

## <span data-ttu-id="bf49b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf49b-132">RELATED LINKS</span></span>

