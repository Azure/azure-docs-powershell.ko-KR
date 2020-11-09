---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310853"
---
# <span data-ttu-id="74937-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74937-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="74937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74937-102">SYNOPSIS</span></span>
<span data-ttu-id="74937-103">Azure application gateway에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74937-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="74937-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74937-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74937-105">설명은</span><span class="sxs-lookup"><span data-stu-id="74937-105">DESCRIPTION</span></span>
<span data-ttu-id="74937-106">Remove-AzApplicationGatewaySslPolicy cmdlet은 Azure 응용 프로그램 게이트웨이에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74937-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="74937-107">예제의</span><span class="sxs-lookup"><span data-stu-id="74937-107">EXAMPLES</span></span>

### <span data-ttu-id="74937-108">예제 1: 응용 프로그램 게이트웨이에서 SSL 정책 제거</span><span class="sxs-lookup"><span data-stu-id="74937-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="74937-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="74937-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="74937-110">변수</span><span class="sxs-lookup"><span data-stu-id="74937-110">PARAMETERS</span></span>

### <span data-ttu-id="74937-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74937-111">-ApplicationGateway</span></span>
<span data-ttu-id="74937-112">이 cmdlet이 SSL 정책을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74937-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="74937-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74937-113">-DefaultProfile</span></span>
<span data-ttu-id="74937-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74937-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74937-115">-Force</span><span class="sxs-lookup"><span data-stu-id="74937-115">-Force</span></span>
<span data-ttu-id="74937-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74937-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74937-117">-확인</span><span class="sxs-lookup"><span data-stu-id="74937-117">-Confirm</span></span>
<span data-ttu-id="74937-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="74937-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74937-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74937-119">-WhatIf</span></span>
<span data-ttu-id="74937-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="74937-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74937-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74937-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74937-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74937-122">CommonParameters</span></span>
<span data-ttu-id="74937-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74937-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74937-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74937-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74937-125">입력</span><span class="sxs-lookup"><span data-stu-id="74937-125">INPUTS</span></span>

### <span data-ttu-id="74937-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74937-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74937-127">출력</span><span class="sxs-lookup"><span data-stu-id="74937-127">OUTPUTS</span></span>

### <span data-ttu-id="74937-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74937-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74937-129">상속자</span><span class="sxs-lookup"><span data-stu-id="74937-129">NOTES</span></span>
<span data-ttu-id="74937-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="74937-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="74937-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74937-131">RELATED LINKS</span></span>

[<span data-ttu-id="74937-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74937-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="74937-133">새로운 AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74937-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="74937-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="74937-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

