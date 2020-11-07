---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: f3b641e3e9229706f3010e7db95480423b06361c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881009"
---
# <span data-ttu-id="30e2e-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30e2e-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="30e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="30e2e-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="30e2e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30e2e-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e2e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30e2e-105">DESCRIPTION</span></span>
<span data-ttu-id="30e2e-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="30e2e-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="30e2e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30e2e-107">EXAMPLES</span></span>

### <span data-ttu-id="30e2e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="30e2e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="30e2e-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="30e2e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="30e2e-110">변수</span><span class="sxs-lookup"><span data-stu-id="30e2e-110">PARAMETERS</span></span>

### <span data-ttu-id="30e2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e2e-111">-DefaultProfile</span></span>
<span data-ttu-id="30e2e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30e2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30e2e-113">-이름</span><span class="sxs-lookup"><span data-stu-id="30e2e-113">-Name</span></span>
<span data-ttu-id="30e2e-114">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30e2e-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e2e-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="30e2e-115">-RouteFilter</span></span>
<span data-ttu-id="30e2e-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="30e2e-116">The RouteFilter</span></span>

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

### <span data-ttu-id="30e2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e2e-117">CommonParameters</span></span>
<span data-ttu-id="30e2e-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e2e-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e2e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e2e-120">입력</span><span class="sxs-lookup"><span data-stu-id="30e2e-120">INPUTS</span></span>

### <span data-ttu-id="30e2e-121">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="30e2e-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="30e2e-122">출력</span><span class="sxs-lookup"><span data-stu-id="30e2e-122">OUTPUTS</span></span>

### <span data-ttu-id="30e2e-123">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="30e2e-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="30e2e-124">상속자</span><span class="sxs-lookup"><span data-stu-id="30e2e-124">NOTES</span></span>

## <span data-ttu-id="30e2e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30e2e-125">RELATED LINKS</span></span>

