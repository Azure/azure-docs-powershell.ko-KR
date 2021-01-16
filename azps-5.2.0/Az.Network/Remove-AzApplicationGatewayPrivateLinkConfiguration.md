---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333926"
---
# <span data-ttu-id="ef32a-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef32a-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ef32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef32a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef32a-103">애플리케이션 게이트웨이에서 privateLink 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ef32a-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="ef32a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef32a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef32a-105">설명</span><span class="sxs-lookup"><span data-stu-id="ef32a-105">DESCRIPTION</span></span>
<span data-ttu-id="ef32a-106">**Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에서 privateLink 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ef32a-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ef32a-107">예제</span><span class="sxs-lookup"><span data-stu-id="ef32a-107">EXAMPLES</span></span>

### <span data-ttu-id="ef32a-108">예제 1: Application Gateway PrivateLink 구성 제거</span><span class="sxs-lookup"><span data-stu-id="ef32a-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="ef32a-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ef32a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ef32a-110">두 번째 명령은 $AppGw.에 저장된 애플리케이션 게이트웨이에서 privateLinkConfig01이라는 privateLink 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ef32a-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ef32a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef32a-111">PARAMETERS</span></span>

### <span data-ttu-id="ef32a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef32a-112">-ApplicationGateway</span></span>
<span data-ttu-id="ef32a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef32a-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef32a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef32a-114">-DefaultProfile</span></span>
<span data-ttu-id="ef32a-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef32a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef32a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ef32a-116">-Name</span></span>
<span data-ttu-id="ef32a-117">Application Gateway privateLink 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="ef32a-117">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef32a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef32a-118">CommonParameters</span></span>
<span data-ttu-id="ef32a-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef32a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef32a-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef32a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef32a-121">입력</span><span class="sxs-lookup"><span data-stu-id="ef32a-121">INPUTS</span></span>

### <span data-ttu-id="ef32a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef32a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef32a-123">출력</span><span class="sxs-lookup"><span data-stu-id="ef32a-123">OUTPUTS</span></span>

### <span data-ttu-id="ef32a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef32a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef32a-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef32a-125">NOTES</span></span>

## <span data-ttu-id="ef32a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef32a-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef32a-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef32a-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ef32a-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef32a-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ef32a-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef32a-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ef32a-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef32a-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)