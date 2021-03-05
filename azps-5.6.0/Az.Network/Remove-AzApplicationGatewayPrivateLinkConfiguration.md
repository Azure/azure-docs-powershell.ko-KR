---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 367e54036d7665cf59ebcc6f1a10b3060b97580d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991018"
---
# <span data-ttu-id="6471c-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6471c-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="6471c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6471c-102">SYNOPSIS</span></span>
<span data-ttu-id="6471c-103">애플리케이션 게이트웨이에서 privateLink 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6471c-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="6471c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6471c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6471c-105">설명</span><span class="sxs-lookup"><span data-stu-id="6471c-105">DESCRIPTION</span></span>
<span data-ttu-id="6471c-106">**Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에서 privateLink 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6471c-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="6471c-107">예제</span><span class="sxs-lookup"><span data-stu-id="6471c-107">EXAMPLES</span></span>

### <span data-ttu-id="6471c-108">예제 1: 애플리케이션 게이트웨이 PrivateLink 구성 제거</span><span class="sxs-lookup"><span data-stu-id="6471c-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="6471c-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6471c-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6471c-110">두 번째 명령은 에 저장된 애플리케이션 게이트웨이에서 privateLinkConfig01이라는 privateLink 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6471c-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6471c-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6471c-111">PARAMETERS</span></span>

### <span data-ttu-id="6471c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6471c-112">-ApplicationGateway</span></span>
<span data-ttu-id="6471c-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6471c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6471c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6471c-114">-DefaultProfile</span></span>
<span data-ttu-id="6471c-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6471c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6471c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6471c-116">-Name</span></span>
<span data-ttu-id="6471c-117">애플리케이션 게이트웨이 privateLink 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="6471c-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="6471c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6471c-118">CommonParameters</span></span>
<span data-ttu-id="6471c-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6471c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6471c-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6471c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6471c-121">입력</span><span class="sxs-lookup"><span data-stu-id="6471c-121">INPUTS</span></span>

### <span data-ttu-id="6471c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6471c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6471c-123">출력</span><span class="sxs-lookup"><span data-stu-id="6471c-123">OUTPUTS</span></span>

### <span data-ttu-id="6471c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6471c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6471c-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6471c-125">NOTES</span></span>

## <span data-ttu-id="6471c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6471c-126">RELATED LINKS</span></span>

[<span data-ttu-id="6471c-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6471c-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6471c-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6471c-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6471c-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6471c-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6471c-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6471c-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)