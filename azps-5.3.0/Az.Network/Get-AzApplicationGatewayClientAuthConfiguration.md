---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492217"
---
# <span data-ttu-id="29a3c-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a3c-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="29a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="29a3c-103">SSL 프로필 개체의 클라이언트 인증 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="29a3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="29a3c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a3c-105">설명</span><span class="sxs-lookup"><span data-stu-id="29a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="29a3c-106">**Get-AzApplicationGatewayClientAuthConfiguration** cmdlet은 SSL 프로필 개체의 클라이언트 인증 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="29a3c-107">예제</span><span class="sxs-lookup"><span data-stu-id="29a3c-107">EXAMPLES</span></span>

### <span data-ttu-id="29a3c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="29a3c-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="29a3c-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="29a3c-110">두 번째 명령은 SslProfile01이라는 SSL 프로필을 $AppGw 변수에 $SslProfile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="29a3c-111">마지막 명령은 SSL 프로필에서 클라이언트 인증 구성을 $SslProfile 변수에 $ClientAuthConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="29a3c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29a3c-112">PARAMETERS</span></span>

### <span data-ttu-id="29a3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a3c-113">-DefaultProfile</span></span>
<span data-ttu-id="29a3c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29a3c-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="29a3c-115">-SslProfile</span></span>
<span data-ttu-id="29a3c-116">ssl 프로필</span><span class="sxs-lookup"><span data-stu-id="29a3c-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29a3c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a3c-117">CommonParameters</span></span>
<span data-ttu-id="29a3c-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29a3c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a3c-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29a3c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a3c-120">입력</span><span class="sxs-lookup"><span data-stu-id="29a3c-120">INPUTS</span></span>

### <span data-ttu-id="29a3c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="29a3c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="29a3c-122">출력</span><span class="sxs-lookup"><span data-stu-id="29a3c-122">OUTPUTS</span></span>

### <span data-ttu-id="29a3c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a3c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="29a3c-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29a3c-124">NOTES</span></span>

## <span data-ttu-id="29a3c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29a3c-125">RELATED LINKS</span></span>

[<span data-ttu-id="29a3c-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a3c-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="29a3c-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a3c-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="29a3c-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a3c-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="29a3c-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a3c-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)