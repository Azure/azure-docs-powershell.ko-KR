---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203161"
---
# <span data-ttu-id="91d96-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="91d96-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="91d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91d96-102">SYNOPSIS</span></span>
<span data-ttu-id="91d96-103">애플리케이션 게이트웨이의 개인 링크 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="91d96-104">구문</span><span class="sxs-lookup"><span data-stu-id="91d96-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91d96-105">설명</span><span class="sxs-lookup"><span data-stu-id="91d96-105">DESCRIPTION</span></span>
<span data-ttu-id="91d96-106">**Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 애플리케이션 게이트웨이의 개인 링크 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="91d96-107">예제</span><span class="sxs-lookup"><span data-stu-id="91d96-107">EXAMPLES</span></span>

### <span data-ttu-id="91d96-108">예제 1: 지정된 개인 링크 구성을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="91d96-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="91d96-110">두 번째 명령은 $AppGw privateLinkConfig01이라는 개인 링크 구성을 $PrivateLinkConfiguration 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="91d96-111">예제 2: 개인 링크 구성 목록 다운로드</span><span class="sxs-lookup"><span data-stu-id="91d96-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="91d96-112">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="91d96-113">두 번째 명령은 $AppGw 모든 개인 링크 구성을 $PrivateLinkConfigurations 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="91d96-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91d96-114">PARAMETERS</span></span>

### <span data-ttu-id="91d96-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91d96-115">-ApplicationGateway</span></span>
<span data-ttu-id="91d96-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91d96-116">The applicationGateway</span></span>

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

### <span data-ttu-id="91d96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d96-117">-DefaultProfile</span></span>
<span data-ttu-id="91d96-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d96-119">-Name</span><span class="sxs-lookup"><span data-stu-id="91d96-119">-Name</span></span>
<span data-ttu-id="91d96-120">Application Gateway privateLink 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="91d96-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="91d96-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d96-121">CommonParameters</span></span>
<span data-ttu-id="91d96-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91d96-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d96-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91d96-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d96-124">입력</span><span class="sxs-lookup"><span data-stu-id="91d96-124">INPUTS</span></span>

### <span data-ttu-id="91d96-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91d96-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91d96-126">출력</span><span class="sxs-lookup"><span data-stu-id="91d96-126">OUTPUTS</span></span>

### <span data-ttu-id="91d96-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="91d96-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="91d96-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91d96-128">NOTES</span></span>

## <span data-ttu-id="91d96-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91d96-129">RELATED LINKS</span></span>

[<span data-ttu-id="91d96-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="91d96-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="91d96-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="91d96-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="91d96-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="91d96-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="91d96-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="91d96-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)