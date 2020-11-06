---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530775"
---
# <span data-ttu-id="63f24-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63f24-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="63f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f24-102">SYNOPSIS</span></span>
<span data-ttu-id="63f24-103">응용 프로그램 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63f24-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63f24-105">DESCRIPTION</span></span>
<span data-ttu-id="63f24-106">**AzureRmApplicationGatewayIPConfiguration** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="63f24-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63f24-107">EXAMPLES</span></span>

### <span data-ttu-id="63f24-108">예제 1: Azure 응용 프로그램 게이트웨이에서 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="63f24-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="63f24-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="63f24-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Subnet02 이라는 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="63f24-111">변수</span><span class="sxs-lookup"><span data-stu-id="63f24-111">PARAMETERS</span></span>

### <span data-ttu-id="63f24-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63f24-112">-ApplicationGateway</span></span>
<span data-ttu-id="63f24-113">IP 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="63f24-114">-이름</span><span class="sxs-lookup"><span data-stu-id="63f24-114">-Name</span></span>
<span data-ttu-id="63f24-115">제거할 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-115">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="63f24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f24-116">-DefaultProfile</span></span>
<span data-ttu-id="63f24-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f24-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f24-118">CommonParameters</span></span>
<span data-ttu-id="63f24-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f24-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f24-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f24-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f24-121">입력</span><span class="sxs-lookup"><span data-stu-id="63f24-121">INPUTS</span></span>

### <span data-ttu-id="63f24-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63f24-122">System.String</span></span>

## <span data-ttu-id="63f24-123">출력</span><span class="sxs-lookup"><span data-stu-id="63f24-123">OUTPUTS</span></span>

### <span data-ttu-id="63f24-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63f24-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63f24-125">상속자</span><span class="sxs-lookup"><span data-stu-id="63f24-125">NOTES</span></span>

## <span data-ttu-id="63f24-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63f24-126">RELATED LINKS</span></span>

[<span data-ttu-id="63f24-127">추가-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63f24-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="63f24-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63f24-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="63f24-129">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63f24-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="63f24-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63f24-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


