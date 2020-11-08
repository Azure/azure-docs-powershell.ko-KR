---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216573"
---
# <span data-ttu-id="e480c-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e480c-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="e480c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e480c-102">SYNOPSIS</span></span>
<span data-ttu-id="e480c-103">응용 프로그램 게이트웨이에 개인 링크 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="e480c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e480c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e480c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e480c-105">DESCRIPTION</span></span>
<span data-ttu-id="e480c-106">**Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 응용 프로그램 게이트웨이에 개인 링크 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="e480c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e480c-107">EXAMPLES</span></span>

### <span data-ttu-id="e480c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e480c-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="e480c-109">첫 번째 명령은 privateLinkIpConfiguration를 만들고이를 $PrivateLinkIpConfiguration 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="e480c-110">두 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e480c-111">세 번째 명령은 privateLinkConfig01 이라는 개인 링크 구성을 해당 게이트웨이에 대해 $AppGw에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="e480c-112">변수</span><span class="sxs-lookup"><span data-stu-id="e480c-112">PARAMETERS</span></span>

### <span data-ttu-id="e480c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e480c-113">-ApplicationGateway</span></span>
<span data-ttu-id="e480c-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e480c-114">The applicationGateway</span></span>

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

### <span data-ttu-id="e480c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e480c-115">-DefaultProfile</span></span>
<span data-ttu-id="e480c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e480c-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e480c-117">-IpConfiguration</span></span>
<span data-ttu-id="e480c-118">IpConfiguration 목록</span><span class="sxs-lookup"><span data-stu-id="e480c-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="e480c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e480c-119">-Name</span></span>
<span data-ttu-id="e480c-120">PrivateLink 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="e480c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e480c-121">CommonParameters</span></span>
<span data-ttu-id="e480c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e480c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e480c-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e480c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e480c-124">입력</span><span class="sxs-lookup"><span data-stu-id="e480c-124">INPUTS</span></span>

### <span data-ttu-id="e480c-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e480c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="e480c-126">PSApplicationGatewayPrivateLinkIpConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="e480c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="e480c-127">출력</span><span class="sxs-lookup"><span data-stu-id="e480c-127">OUTPUTS</span></span>

### <span data-ttu-id="e480c-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e480c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e480c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e480c-129">NOTES</span></span>

## <span data-ttu-id="e480c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e480c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e480c-131">새로운 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e480c-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e480c-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e480c-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e480c-133">제거-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e480c-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="e480c-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e480c-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)