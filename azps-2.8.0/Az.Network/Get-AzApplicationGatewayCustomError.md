---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: fbf10b3cfc323a25a7d7a63dc047a4b24141c5d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870794"
---
# <span data-ttu-id="e48db-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e48db-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e48db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48db-102">SYNOPSIS</span></span>
<span data-ttu-id="e48db-103">응용 프로그램 게이트웨이에서 사용자 지정 오류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="e48db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e48db-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e48db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e48db-105">DESCRIPTION</span></span>
<span data-ttu-id="e48db-106">**AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이에서 사용자 지정 오류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="e48db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e48db-107">EXAMPLES</span></span>

### <span data-ttu-id="e48db-108">예제 1: 응용 프로그램 게이트웨이에서 사용자 지정 오류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="e48db-109">이 명령은 응용 프로그램 게이트웨이에서 $appgw http 상태 코드 502의 사용자 지정 오류를 가져와 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="e48db-110">예제 2: 응용 프로그램 게이트웨이에서 모든 사용자 지정 오류 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="e48db-111">이 명령은 응용 프로그램 게이트웨이에서 $appgw 모든 사용자 지정 오류 목록을 가져와 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="e48db-112">변수</span><span class="sxs-lookup"><span data-stu-id="e48db-112">PARAMETERS</span></span>

### <span data-ttu-id="e48db-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e48db-113">-ApplicationGateway</span></span>
<span data-ttu-id="e48db-114">응용 프로그램 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="e48db-114">The Application Gateway</span></span>

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

### <span data-ttu-id="e48db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48db-115">-DefaultProfile</span></span>
<span data-ttu-id="e48db-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e48db-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e48db-117">-StatusCode</span></span>
<span data-ttu-id="e48db-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e48db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48db-119">CommonParameters</span></span>
<span data-ttu-id="e48db-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e48db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48db-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e48db-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48db-122">입력</span><span class="sxs-lookup"><span data-stu-id="e48db-122">INPUTS</span></span>

### <span data-ttu-id="e48db-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e48db-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e48db-124">출력</span><span class="sxs-lookup"><span data-stu-id="e48db-124">OUTPUTS</span></span>

### <span data-ttu-id="e48db-125">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e48db-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e48db-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e48db-126">NOTES</span></span>

## <span data-ttu-id="e48db-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e48db-127">RELATED LINKS</span></span>

[<span data-ttu-id="e48db-128">추가-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e48db-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e48db-129">새로운 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e48db-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e48db-130">제거-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e48db-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e48db-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e48db-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
