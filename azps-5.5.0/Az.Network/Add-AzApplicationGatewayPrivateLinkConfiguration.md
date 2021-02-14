---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189985"
---
# <span data-ttu-id="ee106-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee106-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ee106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee106-102">SYNOPSIS</span></span>
<span data-ttu-id="ee106-103">애플리케이션 게이트웨이에 개인 링크 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ee106-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="ee106-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee106-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee106-105">설명</span><span class="sxs-lookup"><span data-stu-id="ee106-105">DESCRIPTION</span></span>
<span data-ttu-id="ee106-106">**Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 애플리케이션 게이트웨이에 개인 링크 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ee106-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="ee106-107">예제</span><span class="sxs-lookup"><span data-stu-id="ee106-107">EXAMPLES</span></span>

### <span data-ttu-id="ee106-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee106-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="ee106-109">첫 번째 명령은 privateLinkIpConfiguration을 만들고 $PrivateLinkIpConfiguration 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ee106-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="ee106-110">두 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ee106-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ee106-111">세 번째 명령은 $AppGw</span><span class="sxs-lookup"><span data-stu-id="ee106-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="ee106-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee106-112">PARAMETERS</span></span>

### <span data-ttu-id="ee106-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee106-113">-ApplicationGateway</span></span>
<span data-ttu-id="ee106-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee106-114">The applicationGateway</span></span>

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

### <span data-ttu-id="ee106-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee106-115">-DefaultProfile</span></span>
<span data-ttu-id="ee106-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee106-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee106-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee106-117">-IpConfiguration</span></span>
<span data-ttu-id="ee106-118">ipConfiguration 목록</span><span class="sxs-lookup"><span data-stu-id="ee106-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ee106-119">-Name</span></span>
<span data-ttu-id="ee106-120">privateLink 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="ee106-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="ee106-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee106-121">CommonParameters</span></span>
<span data-ttu-id="ee106-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee106-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee106-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee106-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee106-124">입력</span><span class="sxs-lookup"><span data-stu-id="ee106-124">INPUTS</span></span>

### <span data-ttu-id="ee106-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee106-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="ee106-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ee106-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="ee106-127">출력</span><span class="sxs-lookup"><span data-stu-id="ee106-127">OUTPUTS</span></span>

### <span data-ttu-id="ee106-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee106-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee106-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee106-129">NOTES</span></span>

## <span data-ttu-id="ee106-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee106-130">RELATED LINKS</span></span>

[<span data-ttu-id="ee106-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee106-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ee106-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee106-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ee106-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee106-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ee106-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee106-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)