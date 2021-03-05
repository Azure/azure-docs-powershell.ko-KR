---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 105097f30ea87637cd0ad4bd16e0b8da922c2f4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001168"
---
# <span data-ttu-id="0ce45-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="0ce45-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="0ce45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce45-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce45-103">애플리케이션 게이트웨이에 할당된 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ce45-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="0ce45-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ce45-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ce45-105">설명</span><span class="sxs-lookup"><span data-stu-id="0ce45-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce45-106">**Get-AzApplicationGatewayIdentity** cmdlet은 애플리케이션 게이트웨이에 할당된 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ce45-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="0ce45-107">예제</span><span class="sxs-lookup"><span data-stu-id="0ce45-107">EXAMPLES</span></span>

### <span data-ttu-id="0ce45-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ce45-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="0ce45-109">이 예제에서는 Application Gateway에서 애플리케이션 게이트웨이 ID를 얻을 수 있는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ce45-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="0ce45-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ce45-110">PARAMETERS</span></span>

### <span data-ttu-id="0ce45-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ce45-111">-ApplicationGateway</span></span>
<span data-ttu-id="0ce45-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ce45-112">The applicationGateway</span></span>

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

### <span data-ttu-id="0ce45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce45-113">-DefaultProfile</span></span>
<span data-ttu-id="0ce45-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce45-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce45-115">CommonParameters</span></span>
<span data-ttu-id="0ce45-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce45-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce45-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ce45-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce45-118">입력</span><span class="sxs-lookup"><span data-stu-id="0ce45-118">INPUTS</span></span>

### <span data-ttu-id="0ce45-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ce45-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ce45-120">출력</span><span class="sxs-lookup"><span data-stu-id="0ce45-120">OUTPUTS</span></span>

### <span data-ttu-id="0ce45-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="0ce45-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="0ce45-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ce45-122">NOTES</span></span>

## <span data-ttu-id="0ce45-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ce45-123">RELATED LINKS</span></span>
