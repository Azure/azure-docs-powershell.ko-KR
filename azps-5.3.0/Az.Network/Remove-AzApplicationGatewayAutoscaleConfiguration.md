---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378841"
---
# <span data-ttu-id="7a328-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a328-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7a328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a328-102">SYNOPSIS</span></span>
<span data-ttu-id="7a328-103">애플리케이션 게이트웨이에서 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="7a328-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a328-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a328-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a328-105">DESCRIPTION</span></span>
<span data-ttu-id="7a328-106">**Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet은 기존 Application Gateway에서 자동 크기 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7a328-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a328-107">EXAMPLES</span></span>

### <span data-ttu-id="7a328-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a328-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="7a328-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="7a328-110">두 번째 명령은 애플리케이션 게이트웨이에서 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="7a328-111">세 번째 명령은 Azure에서 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="7a328-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a328-112">PARAMETERS</span></span>

### <span data-ttu-id="7a328-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a328-113">-ApplicationGateway</span></span>
<span data-ttu-id="7a328-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a328-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a328-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a328-115">-DefaultProfile</span></span>
<span data-ttu-id="7a328-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a328-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7a328-117">-Force</span></span>
<span data-ttu-id="7a328-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7a328-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a328-119">-Confirm</span></span>
<span data-ttu-id="7a328-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a328-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a328-121">-WhatIf</span></span>
<span data-ttu-id="7a328-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a328-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a328-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a328-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a328-124">CommonParameters</span></span>
<span data-ttu-id="7a328-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a328-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a328-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a328-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a328-127">입력</span><span class="sxs-lookup"><span data-stu-id="7a328-127">INPUTS</span></span>

### <span data-ttu-id="7a328-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a328-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a328-129">출력</span><span class="sxs-lookup"><span data-stu-id="7a328-129">OUTPUTS</span></span>

### <span data-ttu-id="7a328-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a328-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a328-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a328-131">NOTES</span></span>

## <span data-ttu-id="7a328-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a328-132">RELATED LINKS</span></span>

[<span data-ttu-id="7a328-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a328-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="7a328-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a328-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="7a328-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a328-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
