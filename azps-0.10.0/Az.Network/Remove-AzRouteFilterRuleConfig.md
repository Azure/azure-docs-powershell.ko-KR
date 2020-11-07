---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: bcb0d59c564087e02cd152c1ae76f38c91f33e80
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876649"
---
# <span data-ttu-id="73e66-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73e66-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="73e66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73e66-102">SYNOPSIS</span></span>
<span data-ttu-id="73e66-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="73e66-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="73e66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73e66-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73e66-105">DESCRIPTION</span></span>
<span data-ttu-id="73e66-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="73e66-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="73e66-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73e66-107">EXAMPLES</span></span>

### <span data-ttu-id="73e66-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="73e66-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="73e66-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="73e66-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="73e66-110">변수</span><span class="sxs-lookup"><span data-stu-id="73e66-110">PARAMETERS</span></span>

### <span data-ttu-id="73e66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e66-111">-DefaultProfile</span></span>
<span data-ttu-id="73e66-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73e66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e66-113">-Force</span><span class="sxs-lookup"><span data-stu-id="73e66-113">-Force</span></span>
<span data-ttu-id="73e66-114">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="73e66-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="73e66-115">-이름</span><span class="sxs-lookup"><span data-stu-id="73e66-115">-Name</span></span>
<span data-ttu-id="73e66-116">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73e66-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="73e66-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="73e66-117">-RouteFilter</span></span>
<span data-ttu-id="73e66-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="73e66-118">The RouteFilter</span></span>

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

### <span data-ttu-id="73e66-119">-확인</span><span class="sxs-lookup"><span data-stu-id="73e66-119">-Confirm</span></span>
<span data-ttu-id="73e66-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e66-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e66-121">-WhatIf</span></span>
<span data-ttu-id="73e66-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73e66-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73e66-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73e66-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e66-124">CommonParameters</span></span>
<span data-ttu-id="73e66-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e66-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e66-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e66-127">입력</span><span class="sxs-lookup"><span data-stu-id="73e66-127">INPUTS</span></span>

### <span data-ttu-id="73e66-128">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="73e66-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="73e66-129">출력</span><span class="sxs-lookup"><span data-stu-id="73e66-129">OUTPUTS</span></span>

### <span data-ttu-id="73e66-130">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="73e66-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="73e66-131">상속자</span><span class="sxs-lookup"><span data-stu-id="73e66-131">NOTES</span></span>

## <span data-ttu-id="73e66-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73e66-132">RELATED LINKS</span></span>

