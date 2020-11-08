---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033809"
---
# <span data-ttu-id="6351c-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="6351c-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="6351c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6351c-102">SYNOPSIS</span></span>
<span data-ttu-id="6351c-103">응용 프로그램 게이트웨이에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="6351c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6351c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6351c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6351c-105">DESCRIPTION</span></span>
<span data-ttu-id="6351c-106">**AzApplicationGatewayIdentity** cmdlet은 응용 프로그램 게이트웨이에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="6351c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6351c-107">EXAMPLES</span></span>

### <span data-ttu-id="6351c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6351c-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="6351c-109">이 예제에서는 기존 응용 프로그램 게이트웨이에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="6351c-110">참고: 게이트웨이가 keyvault 비밀을 참조 하는 경우에는이 작업을 통해 해당 ssl 인증서 참조를 제거 하는 것도 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="6351c-111">변수</span><span class="sxs-lookup"><span data-stu-id="6351c-111">PARAMETERS</span></span>

### <span data-ttu-id="6351c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6351c-112">-ApplicationGateway</span></span>
<span data-ttu-id="6351c-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6351c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6351c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6351c-114">-DefaultProfile</span></span>
<span data-ttu-id="6351c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6351c-116">-확인</span><span class="sxs-lookup"><span data-stu-id="6351c-116">-Confirm</span></span>
<span data-ttu-id="6351c-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6351c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6351c-118">-WhatIf</span></span>
<span data-ttu-id="6351c-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6351c-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6351c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6351c-121">CommonParameters</span></span>
<span data-ttu-id="6351c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6351c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6351c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6351c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6351c-124">입력</span><span class="sxs-lookup"><span data-stu-id="6351c-124">INPUTS</span></span>

### <span data-ttu-id="6351c-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6351c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6351c-126">출력</span><span class="sxs-lookup"><span data-stu-id="6351c-126">OUTPUTS</span></span>

### <span data-ttu-id="6351c-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6351c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6351c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="6351c-128">NOTES</span></span>

## <span data-ttu-id="6351c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6351c-129">RELATED LINKS</span></span>