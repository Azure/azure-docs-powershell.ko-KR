---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 002fdabfb01a0b12d36c69b0a8a75ddf91880012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965659"
---
# <span data-ttu-id="ec4fb-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4fb-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="ec4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4fb-103">SSL 프로필에 대한 새 클라이언트 인증 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="ec4fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec4fb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec4fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec4fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4fb-106">**New-AzApplicationGatewayClientAuthConfiguration** cmdlet은 SSL 프로필에 대한 새 클라이언트 인증 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="ec4fb-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec4fb-107">EXAMPLES</span></span>

### <span data-ttu-id="ec4fb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec4fb-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="ec4fb-109">명령은 새 클라이언트 Auth 구성을 만들고 SSL 프로필에 사용할 $clientAuthConfig 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="ec4fb-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec4fb-110">PARAMETERS</span></span>

### <span data-ttu-id="ec4fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4fb-111">-DefaultProfile</span></span>
<span data-ttu-id="ec4fb-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4fb-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="ec4fb-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="ec4fb-114">클라이언트 인증서 발급자 이름을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4fb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4fb-115">CommonParameters</span></span>
<span data-ttu-id="ec4fb-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4fb-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec4fb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4fb-118">입력</span><span class="sxs-lookup"><span data-stu-id="ec4fb-118">INPUTS</span></span>

### <span data-ttu-id="ec4fb-119">없음</span><span class="sxs-lookup"><span data-stu-id="ec4fb-119">None</span></span>

## <span data-ttu-id="ec4fb-120">출력</span><span class="sxs-lookup"><span data-stu-id="ec4fb-120">OUTPUTS</span></span>

### <span data-ttu-id="ec4fb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4fb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="ec4fb-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec4fb-122">NOTES</span></span>

## <span data-ttu-id="ec4fb-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec4fb-123">RELATED LINKS</span></span>

[<span data-ttu-id="ec4fb-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4fb-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="ec4fb-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4fb-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="ec4fb-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4fb-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="ec4fb-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec4fb-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)