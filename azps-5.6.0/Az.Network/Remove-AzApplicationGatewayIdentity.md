---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 7d4cce44aa76628011b35d6723b1ae34a869a2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987728"
---
# <span data-ttu-id="e8f36-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="e8f36-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="e8f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f36-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f36-103">애플리케이션 게이트웨이에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="e8f36-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8f36-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f36-105">설명</span><span class="sxs-lookup"><span data-stu-id="e8f36-105">DESCRIPTION</span></span>
<span data-ttu-id="e8f36-106">**Remove-AzApplicationGatewayIdentity** cmdlet은 애플리케이션 게이트웨이에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="e8f36-107">예제</span><span class="sxs-lookup"><span data-stu-id="e8f36-107">EXAMPLES</span></span>

### <span data-ttu-id="e8f36-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8f36-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="e8f36-109">이 예제에서는 기존 애플리케이션 게이트웨이에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="e8f36-110">참고: 게이트웨이가 keyvault 비밀을 참조하는 경우 이 작업을 따라 해당 ssl 인증서 참조를 제거하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="e8f36-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8f36-111">PARAMETERS</span></span>

### <span data-ttu-id="e8f36-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8f36-112">-ApplicationGateway</span></span>
<span data-ttu-id="e8f36-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8f36-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e8f36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f36-114">-DefaultProfile</span></span>
<span data-ttu-id="e8f36-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f36-116">-확인</span><span class="sxs-lookup"><span data-stu-id="e8f36-116">-Confirm</span></span>
<span data-ttu-id="e8f36-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f36-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f36-118">-WhatIf</span></span>
<span data-ttu-id="e8f36-119">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f36-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f36-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f36-121">CommonParameters</span></span>
<span data-ttu-id="e8f36-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f36-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f36-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8f36-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f36-124">입력</span><span class="sxs-lookup"><span data-stu-id="e8f36-124">INPUTS</span></span>

### <span data-ttu-id="e8f36-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8f36-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8f36-126">출력</span><span class="sxs-lookup"><span data-stu-id="e8f36-126">OUTPUTS</span></span>

### <span data-ttu-id="e8f36-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8f36-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8f36-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8f36-128">NOTES</span></span>

## <span data-ttu-id="e8f36-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8f36-129">RELATED LINKS</span></span>
