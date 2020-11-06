---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531388"
---
# <span data-ttu-id="a6a66-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6a66-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="a6a66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a66-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a66-103">부하 분산 장치에서 아웃 바운드 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6a66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6a66-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6a66-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a66-106">**AzureRmLoadBalancerOutboundRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 아웃 바운드 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="a6a66-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a6a66-107">EXAMPLES</span></span>

### <span data-ttu-id="a6a66-108">예제 1: Azure 부하 분산 장치에서 아웃 바운드 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="a6a66-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="a6a66-109">첫 번째 명령은 제거 하려는 아웃 바운드 규칙 구성과 연결 된 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a6a66-110">두 번째 명령은 연결 된 아웃 바운드 규칙 구성을 부하 분산 장치에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="a6a66-111">세 번째 명령은 부하 분산 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="a6a66-112">변수</span><span class="sxs-lookup"><span data-stu-id="a6a66-112">PARAMETERS</span></span>

### <span data-ttu-id="a6a66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a66-113">-DefaultProfile</span></span>
<span data-ttu-id="a6a66-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a66-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6a66-115">-LoadBalancer</span></span>
<span data-ttu-id="a6a66-116">부하 분산 장치 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-116">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a66-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a6a66-117">-Name</span></span>
<span data-ttu-id="a6a66-118">아웃 바운드 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="a6a66-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="a6a66-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a6a66-119">-Confirm</span></span>
<span data-ttu-id="a6a66-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6a66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a66-121">-WhatIf</span></span>
<span data-ttu-id="a6a66-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a66-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6a66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a66-124">CommonParameters</span></span>
<span data-ttu-id="a6a66-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a66-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a66-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a66-127">입력</span><span class="sxs-lookup"><span data-stu-id="a6a66-127">INPUTS</span></span>

### <span data-ttu-id="a6a66-128">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6a66-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6a66-129">출력</span><span class="sxs-lookup"><span data-stu-id="a6a66-129">OUTPUTS</span></span>

### <span data-ttu-id="a6a66-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6a66-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6a66-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a6a66-131">NOTES</span></span>

## <span data-ttu-id="a6a66-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a66-132">RELATED LINKS</span></span>
