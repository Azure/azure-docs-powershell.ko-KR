---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044088"
---
# <span data-ttu-id="0761d-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0761d-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="0761d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0761d-102">SYNOPSIS</span></span>
<span data-ttu-id="0761d-103">백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="0761d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0761d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0761d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0761d-105">DESCRIPTION</span></span>
<span data-ttu-id="0761d-106">**AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="0761d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0761d-107">EXAMPLES</span></span>

### <span data-ttu-id="0761d-108">예제 1: 응용 프로그램 게이트웨이에서 URL 경로 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="0761d-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="0761d-109">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와 결과를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="0761d-110">두 번째 명령은 응용 프로그램 게이트웨이에서 map01 이라는 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="0761d-111">세 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="0761d-112">변수</span><span class="sxs-lookup"><span data-stu-id="0761d-112">PARAMETERS</span></span>

### <span data-ttu-id="0761d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0761d-113">-ApplicationGateway</span></span>
<span data-ttu-id="0761d-114">이 cmdlet이 URL 경로 맵 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="0761d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0761d-115">-DefaultProfile</span></span>
<span data-ttu-id="0761d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0761d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0761d-117">-Name</span></span>
<span data-ttu-id="0761d-118">이 cmdlet이 백 엔드 서버에서 제거 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="0761d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0761d-119">CommonParameters</span></span>
<span data-ttu-id="0761d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0761d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0761d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0761d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0761d-122">입력</span><span class="sxs-lookup"><span data-stu-id="0761d-122">INPUTS</span></span>

### <span data-ttu-id="0761d-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0761d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0761d-124">출력</span><span class="sxs-lookup"><span data-stu-id="0761d-124">OUTPUTS</span></span>

### <span data-ttu-id="0761d-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0761d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0761d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="0761d-126">NOTES</span></span>

## <span data-ttu-id="0761d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0761d-127">RELATED LINKS</span></span>

[<span data-ttu-id="0761d-128">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0761d-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0761d-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0761d-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0761d-130">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0761d-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0761d-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0761d-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


