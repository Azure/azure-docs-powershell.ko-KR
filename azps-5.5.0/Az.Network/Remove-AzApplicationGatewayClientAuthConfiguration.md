---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 64dc67a59b739ac7cab51c9c4a02fd7a73f8b4cc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407593"
---
# <span data-ttu-id="e2b95-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b95-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="e2b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b95-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b95-103">SSL 프로필 개체의 클라이언트 인증 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b95-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="e2b95-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2b95-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2b95-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2b95-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b95-106">**Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet은 SSL 프로필 개체의 클라이언트 인증 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b95-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="e2b95-107">예제</span><span class="sxs-lookup"><span data-stu-id="e2b95-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b95-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2b95-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="e2b95-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b95-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="e2b95-110">두 번째 명령은 프로필에 대한 Profile01이라는 SSL 프로필을 $AppGw 변수에 $profile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b95-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="e2b95-111">마지막 명령은 클라이언트에 저장된 ssl 프로필의 클라이언트 인증 구성을 $profile.</span><span class="sxs-lookup"><span data-stu-id="e2b95-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="e2b95-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2b95-112">PARAMETERS</span></span>

### <span data-ttu-id="e2b95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b95-113">-DefaultProfile</span></span>
<span data-ttu-id="e2b95-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b95-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="e2b95-115">-SslProfile</span></span>
<span data-ttu-id="e2b95-116">ssl 프로필</span><span class="sxs-lookup"><span data-stu-id="e2b95-116">The ssl profile</span></span>

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

### <span data-ttu-id="e2b95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b95-117">CommonParameters</span></span>
<span data-ttu-id="e2b95-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b95-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2b95-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b95-120">입력</span><span class="sxs-lookup"><span data-stu-id="e2b95-120">INPUTS</span></span>

### <span data-ttu-id="e2b95-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e2b95-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="e2b95-122">출력</span><span class="sxs-lookup"><span data-stu-id="e2b95-122">OUTPUTS</span></span>

### <span data-ttu-id="e2b95-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e2b95-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="e2b95-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2b95-124">NOTES</span></span>

## <span data-ttu-id="e2b95-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2b95-125">RELATED LINKS</span></span>

[<span data-ttu-id="e2b95-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b95-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="e2b95-127">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b95-127">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="e2b95-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b95-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
