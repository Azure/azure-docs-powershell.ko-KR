---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495160"
---
# <span data-ttu-id="ff9c1-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c1-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ff9c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9c1-103">애플리케이션 게이트웨이에 대한 ssl 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="ff9c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff9c1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff9c1-105">설명</span><span class="sxs-lookup"><span data-stu-id="ff9c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ff9c1-106">**Set-AzApplicationGatewaySslProfile** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 ssl 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="ff9c1-107">예제</span><span class="sxs-lookup"><span data-stu-id="ff9c1-107">EXAMPLES</span></span>

### <span data-ttu-id="ff9c1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff9c1-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="ff9c1-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="ff9c1-110">두 번째 명령은 $AppGw 변수에서 애플리케이션 게이트웨이의 ssl 프로필을 업데이트하여 클라이언트 $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="ff9c1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff9c1-111">PARAMETERS</span></span>

### <span data-ttu-id="ff9c1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff9c1-112">-ApplicationGateway</span></span>
<span data-ttu-id="ff9c1-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff9c1-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ff9c1-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff9c1-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="ff9c1-115">클라이언트 인증 구성 설정</span><span class="sxs-lookup"><span data-stu-id="ff9c1-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c1-116">-DefaultProfile</span></span>
<span data-ttu-id="ff9c1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff9c1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ff9c1-118">-Name</span></span>
<span data-ttu-id="ff9c1-119">SSL 프로필의 이름</span><span class="sxs-lookup"><span data-stu-id="ff9c1-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="ff9c1-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="ff9c1-120">-SslPolicy</span></span>
<span data-ttu-id="ff9c1-121">SSL 정책</span><span class="sxs-lookup"><span data-stu-id="ff9c1-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9c1-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="ff9c1-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="ff9c1-123">신뢰할 수 있는 클라이언트 CA 인증서 체인</span><span class="sxs-lookup"><span data-stu-id="ff9c1-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9c1-124">CommonParameters</span></span>
<span data-ttu-id="ff9c1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9c1-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9c1-127">입력</span><span class="sxs-lookup"><span data-stu-id="ff9c1-127">INPUTS</span></span>

### <span data-ttu-id="ff9c1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff9c1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff9c1-129">출력</span><span class="sxs-lookup"><span data-stu-id="ff9c1-129">OUTPUTS</span></span>

### <span data-ttu-id="ff9c1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff9c1-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff9c1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff9c1-131">NOTES</span></span>

## <span data-ttu-id="ff9c1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff9c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="ff9c1-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c1-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="ff9c1-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c1-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="ff9c1-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c1-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="ff9c1-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ff9c1-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)