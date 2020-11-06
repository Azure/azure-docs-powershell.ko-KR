---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: ffd2d6811aa210aa838c7fb623788e11223c34e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534876"
---
# <span data-ttu-id="06e1b-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="06e1b-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="06e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="06e1b-103">응용 프로그램 게이트웨이에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06e1b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06e1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="06e1b-106">**AzureRmApplicationGatewayFrontendIPConfig** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 프런트 엔드 IP를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="06e1b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06e1b-107">EXAMPLES</span></span>

### <span data-ttu-id="06e1b-108">예제 1: 프런트 엔드 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="06e1b-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="06e1b-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="06e1b-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 FrontEndIP02 이라는 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="06e1b-111">변수</span><span class="sxs-lookup"><span data-stu-id="06e1b-111">PARAMETERS</span></span>

### <span data-ttu-id="06e1b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06e1b-112">-ApplicationGateway</span></span>
<span data-ttu-id="06e1b-113">프런트 엔드 IP 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="06e1b-114">-이름</span><span class="sxs-lookup"><span data-stu-id="06e1b-114">-Name</span></span>
<span data-ttu-id="06e1b-115">제거할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-115">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="06e1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e1b-116">-DefaultProfile</span></span>
<span data-ttu-id="06e1b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06e1b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e1b-118">CommonParameters</span></span>
<span data-ttu-id="06e1b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e1b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e1b-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e1b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e1b-121">입력</span><span class="sxs-lookup"><span data-stu-id="06e1b-121">INPUTS</span></span>

### <span data-ttu-id="06e1b-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06e1b-122">System.String</span></span>

## <span data-ttu-id="06e1b-123">출력</span><span class="sxs-lookup"><span data-stu-id="06e1b-123">OUTPUTS</span></span>

### <span data-ttu-id="06e1b-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06e1b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06e1b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="06e1b-125">NOTES</span></span>

## <span data-ttu-id="06e1b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06e1b-126">RELATED LINKS</span></span>

[<span data-ttu-id="06e1b-127">추가-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="06e1b-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="06e1b-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="06e1b-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="06e1b-129">새로운 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="06e1b-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="06e1b-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="06e1b-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


