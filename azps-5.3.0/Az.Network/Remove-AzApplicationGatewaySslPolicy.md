---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385358"
---
# <span data-ttu-id="0da69-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0da69-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="0da69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da69-102">SYNOPSIS</span></span>
<span data-ttu-id="0da69-103">Azure 애플리케이션 게이트웨이에서 SSL 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="0da69-104">구문</span><span class="sxs-lookup"><span data-stu-id="0da69-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da69-105">설명</span><span class="sxs-lookup"><span data-stu-id="0da69-105">DESCRIPTION</span></span>
<span data-ttu-id="0da69-106">이 Remove-AzApplicationGatewaySslPolicy cmdlet은 Azure 애플리케이션 게이트웨이에서 SSL 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="0da69-107">예제</span><span class="sxs-lookup"><span data-stu-id="0da69-107">EXAMPLES</span></span>

### <span data-ttu-id="0da69-108">예제 1: 애플리케이션 게이트웨이에서 SSL 정책 제거</span><span class="sxs-lookup"><span data-stu-id="0da69-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="0da69-109">이 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이에서 SSL 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="0da69-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0da69-110">PARAMETERS</span></span>

### <span data-ttu-id="0da69-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0da69-111">-ApplicationGateway</span></span>
<span data-ttu-id="0da69-112">이 cmdlet이 SSL 정책을 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="0da69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da69-113">-DefaultProfile</span></span>
<span data-ttu-id="0da69-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da69-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0da69-115">-Force</span></span>
<span data-ttu-id="0da69-116">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0da69-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0da69-117">-Confirm</span></span>
<span data-ttu-id="0da69-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da69-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da69-119">-WhatIf</span></span>
<span data-ttu-id="0da69-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0da69-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da69-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da69-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da69-122">CommonParameters</span></span>
<span data-ttu-id="0da69-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0da69-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da69-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0da69-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da69-125">입력</span><span class="sxs-lookup"><span data-stu-id="0da69-125">INPUTS</span></span>

### <span data-ttu-id="0da69-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0da69-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0da69-127">출력</span><span class="sxs-lookup"><span data-stu-id="0da69-127">OUTPUTS</span></span>

### <span data-ttu-id="0da69-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0da69-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0da69-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0da69-129">NOTES</span></span>
<span data-ttu-id="0da69-130">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="0da69-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0da69-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0da69-131">RELATED LINKS</span></span>

[<span data-ttu-id="0da69-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0da69-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="0da69-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0da69-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="0da69-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0da69-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

