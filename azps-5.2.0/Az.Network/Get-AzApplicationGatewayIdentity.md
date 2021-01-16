---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326234"
---
# <span data-ttu-id="a76fb-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a76fb-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a76fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a76fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a76fb-103">애플리케이션 게이트웨이에 할당된 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a76fb-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a76fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="a76fb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a76fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="a76fb-105">DESCRIPTION</span></span>
<span data-ttu-id="a76fb-106">**Get-AzApplicationGatewayIdentity** cmdlet은 애플리케이션 게이트웨이에 할당된 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a76fb-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a76fb-107">예제</span><span class="sxs-lookup"><span data-stu-id="a76fb-107">EXAMPLES</span></span>

### <span data-ttu-id="a76fb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a76fb-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="a76fb-109">이 예제에서는 Application Gateway에서 애플리케이션 게이트웨이 ID를 얻을 수 있는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a76fb-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="a76fb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a76fb-110">PARAMETERS</span></span>

### <span data-ttu-id="a76fb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a76fb-111">-ApplicationGateway</span></span>
<span data-ttu-id="a76fb-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a76fb-112">The applicationGateway</span></span>

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

### <span data-ttu-id="a76fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76fb-113">-DefaultProfile</span></span>
<span data-ttu-id="a76fb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a76fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a76fb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76fb-115">CommonParameters</span></span>
<span data-ttu-id="a76fb-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a76fb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76fb-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a76fb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76fb-118">입력</span><span class="sxs-lookup"><span data-stu-id="a76fb-118">INPUTS</span></span>

### <span data-ttu-id="a76fb-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a76fb-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a76fb-120">출력</span><span class="sxs-lookup"><span data-stu-id="a76fb-120">OUTPUTS</span></span>

### <span data-ttu-id="a76fb-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a76fb-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="a76fb-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a76fb-122">NOTES</span></span>

## <span data-ttu-id="a76fb-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a76fb-123">RELATED LINKS</span></span>
