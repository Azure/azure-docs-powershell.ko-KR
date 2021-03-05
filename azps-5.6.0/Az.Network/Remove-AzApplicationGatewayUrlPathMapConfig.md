---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1d9caf3c95d7f8a508a41b8c047684b86c66227a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996436"
---
# <span data-ttu-id="ffcbd-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ffcbd-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="ffcbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcbd-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcbd-103">백던드 서버 풀에 대한 URL 경로 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ffcbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="ffcbd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffcbd-105">설명</span><span class="sxs-lookup"><span data-stu-id="ffcbd-105">DESCRIPTION</span></span>
<span data-ttu-id="ffcbd-106">**Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백end 서버 풀에 대한 URL 경로 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ffcbd-107">예제</span><span class="sxs-lookup"><span data-stu-id="ffcbd-107">EXAMPLES</span></span>

### <span data-ttu-id="ffcbd-108">예제 1: 애플리케이션 게이트웨이에서 URL 경로 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="ffcbd-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="ffcbd-109">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 얻게 하여 결과를 $appgw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="ffcbd-110">두 번째 명령은 애플리케이션 게이트웨이에서 map01이라는 URL 경로 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="ffcbd-111">세 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="ffcbd-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ffcbd-112">PARAMETERS</span></span>

### <span data-ttu-id="ffcbd-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffcbd-113">-ApplicationGateway</span></span>
<span data-ttu-id="ffcbd-114">이 cmdlet에서 URL 경로 맵 구성을 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="ffcbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcbd-115">-DefaultProfile</span></span>
<span data-ttu-id="ffcbd-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffcbd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ffcbd-117">-Name</span></span>
<span data-ttu-id="ffcbd-118">이 cmdlet이 백end 서버에서 제거하는 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="ffcbd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcbd-119">CommonParameters</span></span>
<span data-ttu-id="ffcbd-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcbd-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ffcbd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcbd-122">입력</span><span class="sxs-lookup"><span data-stu-id="ffcbd-122">INPUTS</span></span>

### <span data-ttu-id="ffcbd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffcbd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ffcbd-124">출력</span><span class="sxs-lookup"><span data-stu-id="ffcbd-124">OUTPUTS</span></span>

### <span data-ttu-id="ffcbd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffcbd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ffcbd-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ffcbd-126">NOTES</span></span>

## <span data-ttu-id="ffcbd-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffcbd-127">RELATED LINKS</span></span>

[<span data-ttu-id="ffcbd-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ffcbd-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ffcbd-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ffcbd-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ffcbd-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ffcbd-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ffcbd-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ffcbd-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


