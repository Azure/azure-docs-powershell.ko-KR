---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212506"
---
# <span data-ttu-id="8b1f7-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1f7-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="8b1f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1f7-103">응용 프로그램 게이트웨이의 개인 링크 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="8b1f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b1f7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b1f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b1f7-105">DESCRIPTION</span></span>
<span data-ttu-id="8b1f7-106">**Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 응용 프로그램 게이트웨이의 개인 링크 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="8b1f7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b1f7-107">EXAMPLES</span></span>

### <span data-ttu-id="8b1f7-108">예제 1: 지정 된 비공개 링크 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b1f7-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8b1f7-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8b1f7-110">두 번째 명령은 $AppGw에서 privateLinkConfig01 이라는 개인 링크 구성을 가져와 $PrivateLinkConfiguration 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="8b1f7-111">예제 2: 비공개 링크 구성 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b1f7-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="8b1f7-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8b1f7-113">두 번째 명령은 $AppGw에서 모든 개인 링크 구성을 가져와 $PrivateLinkConfigurations 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="8b1f7-114">변수</span><span class="sxs-lookup"><span data-stu-id="8b1f7-114">PARAMETERS</span></span>

### <span data-ttu-id="8b1f7-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b1f7-115">-ApplicationGateway</span></span>
<span data-ttu-id="8b1f7-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b1f7-116">The applicationGateway</span></span>

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

### <span data-ttu-id="8b1f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1f7-117">-DefaultProfile</span></span>
<span data-ttu-id="8b1f7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b1f7-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8b1f7-119">-Name</span></span>
<span data-ttu-id="8b1f7-120">Application gateway privateLink configuration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-120">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b1f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1f7-121">CommonParameters</span></span>
<span data-ttu-id="8b1f7-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1f7-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1f7-124">입력</span><span class="sxs-lookup"><span data-stu-id="8b1f7-124">INPUTS</span></span>

### <span data-ttu-id="8b1f7-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b1f7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b1f7-126">출력</span><span class="sxs-lookup"><span data-stu-id="8b1f7-126">OUTPUTS</span></span>

### <span data-ttu-id="8b1f7-127">PSApplicationGatewayPrivateLinkConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8b1f7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="8b1f7-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8b1f7-128">NOTES</span></span>

## <span data-ttu-id="8b1f7-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b1f7-129">RELATED LINKS</span></span>

[<span data-ttu-id="8b1f7-130">새로운 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1f7-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8b1f7-131">추가-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1f7-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8b1f7-132">제거-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1f7-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8b1f7-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b1f7-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)