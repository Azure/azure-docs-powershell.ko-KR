---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702918"
---
# <span data-ttu-id="a40f3-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a40f3-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="a40f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a40f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a40f3-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="a40f3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a40f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a40f3-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a40f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a40f3-105">DESCRIPTION</span></span>
<span data-ttu-id="a40f3-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="a40f3-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="a40f3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a40f3-107">EXAMPLES</span></span>

### <span data-ttu-id="a40f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a40f3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a40f3-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="a40f3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="a40f3-110">변수</span><span class="sxs-lookup"><span data-stu-id="a40f3-110">PARAMETERS</span></span>

### <span data-ttu-id="a40f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a40f3-111">-AsJob</span></span>
<span data-ttu-id="a40f3-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a40f3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a40f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40f3-113">-DefaultProfile</span></span>
<span data-ttu-id="a40f3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a40f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a40f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a40f3-115">-Force</span></span>
<span data-ttu-id="a40f3-116">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="a40f3-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="a40f3-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a40f3-117">-RouteFilter</span></span>
<span data-ttu-id="a40f3-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a40f3-118">The RouteFilter</span></span>

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

### <span data-ttu-id="a40f3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a40f3-119">-Confirm</span></span>
<span data-ttu-id="a40f3-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40f3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a40f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a40f3-121">-WhatIf</span></span>
<span data-ttu-id="a40f3-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a40f3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a40f3-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a40f3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a40f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40f3-124">CommonParameters</span></span>
<span data-ttu-id="a40f3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40f3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40f3-127">입력</span><span class="sxs-lookup"><span data-stu-id="a40f3-127">INPUTS</span></span>

### <span data-ttu-id="a40f3-128">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a40f3-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="a40f3-129">매개 변수: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a40f3-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="a40f3-130">출력</span><span class="sxs-lookup"><span data-stu-id="a40f3-130">OUTPUTS</span></span>

### <span data-ttu-id="a40f3-131">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a40f3-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a40f3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a40f3-132">NOTES</span></span>

## <span data-ttu-id="a40f3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a40f3-133">RELATED LINKS</span></span>
