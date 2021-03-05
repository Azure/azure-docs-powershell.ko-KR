---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 92e094576306707bb2a3c0533cb6863581163393
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993958"
---
# <span data-ttu-id="3fd9f-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3fd9f-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="3fd9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd9f-103">애플리케이션 게이트웨이 SSL 프로필의 SSL 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="3fd9f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fd9f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd9f-105">설명</span><span class="sxs-lookup"><span data-stu-id="3fd9f-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd9f-106">**Get-AzApplicationGatewaySslProfilePolicy** cmdlet은 애플리케이션 게이트웨이 SSL 프로필의 SSL 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="3fd9f-107">예제</span><span class="sxs-lookup"><span data-stu-id="3fd9f-107">EXAMPLES</span></span>

### <span data-ttu-id="3fd9f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fd9f-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="3fd9f-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="3fd9f-110">두 번째 명령은 SslProfile01이라는 SSL 프로필을 $AppGw 변수에 $SslProfile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="3fd9f-111">마지막 명령은 SSL 프로필에서 SSL 정책을 $SslProfile 및 $sslpolicy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="3fd9f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3fd9f-112">PARAMETERS</span></span>

### <span data-ttu-id="3fd9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd9f-113">-DefaultProfile</span></span>
<span data-ttu-id="3fd9f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd9f-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="3fd9f-115">-SslProfile</span></span>
<span data-ttu-id="3fd9f-116">애플리케이션 게이트웨이 SSL 프로필</span><span class="sxs-lookup"><span data-stu-id="3fd9f-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="3fd9f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd9f-117">CommonParameters</span></span>
<span data-ttu-id="3fd9f-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd9f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd9f-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fd9f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd9f-120">입력</span><span class="sxs-lookup"><span data-stu-id="3fd9f-120">INPUTS</span></span>

### <span data-ttu-id="3fd9f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3fd9f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3fd9f-122">출력</span><span class="sxs-lookup"><span data-stu-id="3fd9f-122">OUTPUTS</span></span>

### <span data-ttu-id="3fd9f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3fd9f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3fd9f-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fd9f-124">NOTES</span></span>

## <span data-ttu-id="3fd9f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fd9f-125">RELATED LINKS</span></span>

[<span data-ttu-id="3fd9f-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3fd9f-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="3fd9f-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3fd9f-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="3fd9f-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3fd9f-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="3fd9f-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3fd9f-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)