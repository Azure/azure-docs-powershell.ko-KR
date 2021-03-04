---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: bfa5cbfdb8ab734a8c6ca8b651808213b9b10f3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958112"
---
# <span data-ttu-id="120a2-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="120a2-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="120a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120a2-102">SYNOPSIS</span></span>
<span data-ttu-id="120a2-103">애플리케이션 게이트웨이의 자동 조정 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="120a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="120a2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120a2-105">설명</span><span class="sxs-lookup"><span data-stu-id="120a2-105">DESCRIPTION</span></span>
<span data-ttu-id="120a2-106">**Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet은 Application Gateway의 기존 자동 크기 조정 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="120a2-107">예제</span><span class="sxs-lookup"><span data-stu-id="120a2-107">EXAMPLES</span></span>

### <span data-ttu-id="120a2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="120a2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="120a2-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 변수에 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="120a2-110">두 번째 명령은 애플리케이션 게이트웨이에서 자동 조정 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="120a2-111">세 번째 명령은 Azure에서 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="120a2-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="120a2-112">PARAMETERS</span></span>

### <span data-ttu-id="120a2-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="120a2-113">-ApplicationGateway</span></span>
<span data-ttu-id="120a2-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="120a2-114">The applicationGateway</span></span>

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

### <span data-ttu-id="120a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120a2-115">-DefaultProfile</span></span>
<span data-ttu-id="120a2-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="120a2-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="120a2-117">-MaxCapacity</span></span>
<span data-ttu-id="120a2-118">애플리케이션 게이트웨이의 최대 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a2-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="120a2-119">-MinCapacity</span></span>
<span data-ttu-id="120a2-120">애플리케이션 게이트웨이에 대한 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a2-121">-확인</span><span class="sxs-lookup"><span data-stu-id="120a2-121">-Confirm</span></span>
<span data-ttu-id="120a2-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120a2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120a2-123">-WhatIf</span></span>
<span data-ttu-id="120a2-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120a2-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120a2-126">CommonParameters</span></span>
<span data-ttu-id="120a2-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="120a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120a2-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="120a2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120a2-129">입력</span><span class="sxs-lookup"><span data-stu-id="120a2-129">INPUTS</span></span>

### <span data-ttu-id="120a2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="120a2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="120a2-131">출력</span><span class="sxs-lookup"><span data-stu-id="120a2-131">OUTPUTS</span></span>

### <span data-ttu-id="120a2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="120a2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="120a2-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="120a2-133">NOTES</span></span>

## <span data-ttu-id="120a2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="120a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="120a2-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="120a2-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="120a2-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="120a2-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="120a2-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="120a2-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
