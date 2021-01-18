---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495176"
---
# <span data-ttu-id="9aa15-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9aa15-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9aa15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aa15-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa15-103">백end 서버 풀에 대한 URL 경로 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9aa15-104">구문</span><span class="sxs-lookup"><span data-stu-id="9aa15-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aa15-105">설명</span><span class="sxs-lookup"><span data-stu-id="9aa15-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa15-106">**Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백end 서버 풀에 대한 URL 경로 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9aa15-107">예제</span><span class="sxs-lookup"><span data-stu-id="9aa15-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa15-108">예제 1: 애플리케이션 게이트웨이에서 URL 경로 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="9aa15-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="9aa15-109">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 다운로드하고 결과를 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="9aa15-110">두 번째 명령은 애플리케이션 게이트웨이에서 map01이라는 URL 경로 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="9aa15-111">세 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="9aa15-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9aa15-112">PARAMETERS</span></span>

### <span data-ttu-id="9aa15-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9aa15-113">-ApplicationGateway</span></span>
<span data-ttu-id="9aa15-114">이 cmdlet이 URL 경로 맵 구성을 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="9aa15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa15-115">-DefaultProfile</span></span>
<span data-ttu-id="9aa15-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aa15-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9aa15-117">-Name</span></span>
<span data-ttu-id="9aa15-118">이 cmdlet이 백end 서버에서 제거하는 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="9aa15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa15-119">CommonParameters</span></span>
<span data-ttu-id="9aa15-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa15-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9aa15-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa15-122">입력</span><span class="sxs-lookup"><span data-stu-id="9aa15-122">INPUTS</span></span>

### <span data-ttu-id="9aa15-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9aa15-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9aa15-124">출력</span><span class="sxs-lookup"><span data-stu-id="9aa15-124">OUTPUTS</span></span>

### <span data-ttu-id="9aa15-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9aa15-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9aa15-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9aa15-126">NOTES</span></span>

## <span data-ttu-id="9aa15-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aa15-127">RELATED LINKS</span></span>

[<span data-ttu-id="9aa15-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9aa15-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9aa15-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9aa15-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9aa15-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9aa15-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9aa15-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9aa15-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


