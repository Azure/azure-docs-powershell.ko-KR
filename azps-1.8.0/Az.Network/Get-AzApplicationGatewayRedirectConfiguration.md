---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 79a4e76f4c9ece74c25c8f017fab6840aac63a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700641"
---
# <span data-ttu-id="e14b2-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14b2-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e14b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e14b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e14b2-103">응용 프로그램 게이트웨이에서 기존 리디렉션 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="e14b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e14b2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e14b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e14b2-105">DESCRIPTION</span></span>
<span data-ttu-id="e14b2-106">**Get-AzApplicationGatewayRedirectConfiguration** Cmdlet은 응용 프로그램 게이트웨이에서 기존 리디렉션 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="e14b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e14b2-107">EXAMPLES</span></span>

### <span data-ttu-id="e14b2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e14b2-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="e14b2-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e14b2-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 Redirect01 이라는 리디렉션 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="e14b2-111">변수</span><span class="sxs-lookup"><span data-stu-id="e14b2-111">PARAMETERS</span></span>

### <span data-ttu-id="e14b2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e14b2-112">-ApplicationGateway</span></span>
<span data-ttu-id="e14b2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e14b2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e14b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14b2-114">-DefaultProfile</span></span>
<span data-ttu-id="e14b2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e14b2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e14b2-116">-Name</span></span>
<span data-ttu-id="e14b2-117">요청 라우팅 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-117">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14b2-118">CommonParameters</span></span>
<span data-ttu-id="e14b2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e14b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14b2-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e14b2-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14b2-121">입력</span><span class="sxs-lookup"><span data-stu-id="e14b2-121">INPUTS</span></span>

### <span data-ttu-id="e14b2-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e14b2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e14b2-123">출력</span><span class="sxs-lookup"><span data-stu-id="e14b2-123">OUTPUTS</span></span>

### <span data-ttu-id="e14b2-124">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="e14b2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e14b2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="e14b2-125">NOTES</span></span>

## <span data-ttu-id="e14b2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e14b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="e14b2-127">추가-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14b2-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e14b2-128">새로운 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14b2-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e14b2-129">제거-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14b2-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e14b2-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e14b2-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
