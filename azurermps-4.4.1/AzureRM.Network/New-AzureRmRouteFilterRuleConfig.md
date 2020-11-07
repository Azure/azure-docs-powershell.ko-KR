---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3c3e20762bcf8e48fc3f01d750419493a81ca8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702435"
---
# <span data-ttu-id="f90a4-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f90a4-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f90a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f90a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f90a4-103">경로 필터에 대 한 경로 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f90a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f90a4-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f90a4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f90a4-105">DESCRIPTION</span></span>
<span data-ttu-id="f90a4-106">New-AzureRmRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 대 한 경로 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="f90a4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f90a4-107">EXAMPLES</span></span>

### <span data-ttu-id="f90a4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f90a4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f90a4-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="f90a4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f90a4-110">변수</span><span class="sxs-lookup"><span data-stu-id="f90a4-110">PARAMETERS</span></span>

### <span data-ttu-id="f90a4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="f90a4-111">-Access</span></span>
<span data-ttu-id="f90a4-112">경로 필터 규칙에 대 한 액세스입니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-112">Access for route filter rule.</span></span>
<span data-ttu-id="f90a4-113">유효한 값은 허용 또는 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="f90a4-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f90a4-114">-CommunityList</span></span>
<span data-ttu-id="f90a4-115">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="f90a4-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="f90a4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f90a4-116">-Force</span></span>
<span data-ttu-id="f90a4-117">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="f90a4-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="f90a4-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f90a4-118">-Name</span></span>
<span data-ttu-id="f90a4-119">경로 필터 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-119">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="f90a4-120">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f90a4-120">-RouteFilterRuleType</span></span>
<span data-ttu-id="f90a4-121">경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-121">Route Filter Rule Type.</span></span>
<span data-ttu-id="f90a4-122">유효한 값은 다음과 같습니다. 커뮤니티</span><span class="sxs-lookup"><span data-stu-id="f90a4-122">Valid values are: Community</span></span>

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

### <span data-ttu-id="f90a4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="f90a4-123">-Confirm</span></span>
<span data-ttu-id="f90a4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f90a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f90a4-125">-WhatIf</span></span>
<span data-ttu-id="f90a4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f90a4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f90a4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90a4-128">-DefaultProfile</span></span>
<span data-ttu-id="f90a4-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f90a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90a4-130">CommonParameters</span></span>
<span data-ttu-id="f90a4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f90a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90a4-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f90a4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90a4-133">입력</span><span class="sxs-lookup"><span data-stu-id="f90a4-133">INPUTS</span></span>

## <span data-ttu-id="f90a4-134">출력</span><span class="sxs-lookup"><span data-stu-id="f90a4-134">OUTPUTS</span></span>

### <span data-ttu-id="f90a4-135">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f90a4-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="f90a4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f90a4-136">NOTES</span></span>
<span data-ttu-id="f90a4-137">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="f90a4-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f90a4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f90a4-138">RELATED LINKS</span></span>

[<span data-ttu-id="f90a4-139">추가-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f90a4-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f90a4-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f90a4-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f90a4-141">제거-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f90a4-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f90a4-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f90a4-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

