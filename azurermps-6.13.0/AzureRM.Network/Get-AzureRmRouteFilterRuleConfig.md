---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 96122c68317166f078d40be8cee9d0124c4d713e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702598"
---
# <span data-ttu-id="5ec04-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5ec04-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="5ec04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ec04-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec04-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="5ec04-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ec04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ec04-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ec04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ec04-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec04-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="5ec04-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="5ec04-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5ec04-107">EXAMPLES</span></span>

### <span data-ttu-id="5ec04-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ec04-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5ec04-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="5ec04-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5ec04-110">변수</span><span class="sxs-lookup"><span data-stu-id="5ec04-110">PARAMETERS</span></span>

### <span data-ttu-id="5ec04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec04-111">-DefaultProfile</span></span>
<span data-ttu-id="5ec04-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ec04-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5ec04-113">-Name</span></span>
<span data-ttu-id="5ec04-114">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec04-114">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec04-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ec04-115">-RouteFilter</span></span>
<span data-ttu-id="5ec04-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5ec04-116">The RouteFilter</span></span>

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

### <span data-ttu-id="5ec04-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec04-117">CommonParameters</span></span>
<span data-ttu-id="5ec04-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec04-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec04-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec04-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec04-120">입력</span><span class="sxs-lookup"><span data-stu-id="5ec04-120">INPUTS</span></span>

### <span data-ttu-id="5ec04-121">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5ec04-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="5ec04-122">매개 변수: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ec04-122">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="5ec04-123">출력</span><span class="sxs-lookup"><span data-stu-id="5ec04-123">OUTPUTS</span></span>

### <span data-ttu-id="5ec04-124">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5ec04-124">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="5ec04-125">상속자</span><span class="sxs-lookup"><span data-stu-id="5ec04-125">NOTES</span></span>

## <span data-ttu-id="5ec04-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ec04-126">RELATED LINKS</span></span>
