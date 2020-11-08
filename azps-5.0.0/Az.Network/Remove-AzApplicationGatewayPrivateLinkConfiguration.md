---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218823"
---
# <span data-ttu-id="77a75-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="77a75-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="77a75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77a75-102">SYNOPSIS</span></span>
<span data-ttu-id="77a75-103">응용 프로그램 게이트웨이에서 privateLink 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="77a75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77a75-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77a75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="77a75-105">DESCRIPTION</span></span>
<span data-ttu-id="77a75-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet은 Azure application Gateway에서 privateLink 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="77a75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="77a75-107">EXAMPLES</span></span>

### <span data-ttu-id="77a75-108">예제 1: 응용 프로그램 게이트웨이 PrivateLink 구성 제거</span><span class="sxs-lookup"><span data-stu-id="77a75-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="77a75-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="77a75-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 privateLinkConfig01 이라는 privateLink 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="77a75-111">변수</span><span class="sxs-lookup"><span data-stu-id="77a75-111">PARAMETERS</span></span>

### <span data-ttu-id="77a75-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77a75-112">-ApplicationGateway</span></span>
<span data-ttu-id="77a75-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77a75-113">The applicationGateway</span></span>

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

### <span data-ttu-id="77a75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a75-114">-DefaultProfile</span></span>
<span data-ttu-id="77a75-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77a75-116">-이름</span><span class="sxs-lookup"><span data-stu-id="77a75-116">-Name</span></span>
<span data-ttu-id="77a75-117">Application gateway privateLink configuration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="77a75-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a75-118">CommonParameters</span></span>
<span data-ttu-id="77a75-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a75-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a75-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77a75-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a75-121">입력</span><span class="sxs-lookup"><span data-stu-id="77a75-121">INPUTS</span></span>

### <span data-ttu-id="77a75-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77a75-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77a75-123">출력</span><span class="sxs-lookup"><span data-stu-id="77a75-123">OUTPUTS</span></span>

### <span data-ttu-id="77a75-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77a75-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77a75-125">상속자</span><span class="sxs-lookup"><span data-stu-id="77a75-125">NOTES</span></span>

## <span data-ttu-id="77a75-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77a75-126">RELATED LINKS</span></span>

[<span data-ttu-id="77a75-127">새로운 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="77a75-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="77a75-128">추가-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="77a75-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="77a75-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="77a75-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="77a75-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="77a75-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)