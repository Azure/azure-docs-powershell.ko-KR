---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700205"
---
# <span data-ttu-id="1045d-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1045d-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1045d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1045d-102">SYNOPSIS</span></span>
<span data-ttu-id="1045d-103">기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="1045d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1045d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1045d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1045d-105">DESCRIPTION</span></span>
<span data-ttu-id="1045d-106">**AzApplicationGatewayRedirectConfiguration** cmdlet은 기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="1045d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1045d-107">EXAMPLES</span></span>

### <span data-ttu-id="1045d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1045d-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="1045d-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1045d-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Redirect01 이라는 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1045d-111">변수</span><span class="sxs-lookup"><span data-stu-id="1045d-111">PARAMETERS</span></span>

### <span data-ttu-id="1045d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1045d-112">-ApplicationGateway</span></span>
<span data-ttu-id="1045d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1045d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1045d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1045d-114">-DefaultProfile</span></span>
<span data-ttu-id="1045d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1045d-116">-이름</span><span class="sxs-lookup"><span data-stu-id="1045d-116">-Name</span></span>
<span data-ttu-id="1045d-117">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-117">The name of the redirect configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1045d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1045d-118">CommonParameters</span></span>
<span data-ttu-id="1045d-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1045d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1045d-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1045d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1045d-121">입력</span><span class="sxs-lookup"><span data-stu-id="1045d-121">INPUTS</span></span>

### <span data-ttu-id="1045d-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1045d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1045d-123">출력</span><span class="sxs-lookup"><span data-stu-id="1045d-123">OUTPUTS</span></span>

### <span data-ttu-id="1045d-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1045d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1045d-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1045d-125">NOTES</span></span>

## <span data-ttu-id="1045d-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1045d-126">RELATED LINKS</span></span>

[<span data-ttu-id="1045d-127">추가-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1045d-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="1045d-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1045d-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="1045d-129">새로운 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1045d-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="1045d-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1045d-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
