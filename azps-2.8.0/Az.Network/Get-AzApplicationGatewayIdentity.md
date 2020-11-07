---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870269"
---
# <span data-ttu-id="deea1-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="deea1-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="deea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deea1-102">SYNOPSIS</span></span>
<span data-ttu-id="deea1-103">응용 프로그램 게이트웨이에 할당 된 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="deea1-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="deea1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="deea1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deea1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="deea1-105">DESCRIPTION</span></span>
<span data-ttu-id="deea1-106">**AzApplicationGatewayIdentity** cmdlet은 응용 프로그램 게이트웨이에 할당 된 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="deea1-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="deea1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="deea1-107">EXAMPLES</span></span>

### <span data-ttu-id="deea1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="deea1-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="deea1-109">이 예제에서는 Application Gateway에서 응용 프로그램 게이트웨이 id를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="deea1-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="deea1-110">변수</span><span class="sxs-lookup"><span data-stu-id="deea1-110">PARAMETERS</span></span>

### <span data-ttu-id="deea1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deea1-111">-ApplicationGateway</span></span>
<span data-ttu-id="deea1-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deea1-112">The applicationGateway</span></span>

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

### <span data-ttu-id="deea1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deea1-113">-DefaultProfile</span></span>
<span data-ttu-id="deea1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="deea1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deea1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deea1-115">CommonParameters</span></span>
<span data-ttu-id="deea1-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="deea1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deea1-117">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="deea1-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deea1-118">입력</span><span class="sxs-lookup"><span data-stu-id="deea1-118">INPUTS</span></span>

### <span data-ttu-id="deea1-119">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deea1-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="deea1-120">출력</span><span class="sxs-lookup"><span data-stu-id="deea1-120">OUTPUTS</span></span>

### <span data-ttu-id="deea1-121">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="deea1-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="deea1-122">상속자</span><span class="sxs-lookup"><span data-stu-id="deea1-122">NOTES</span></span>

## <span data-ttu-id="deea1-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="deea1-123">RELATED LINKS</span></span>
