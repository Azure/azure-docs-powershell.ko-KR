---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ab8afdb01a2993330c75b23b02392ee583cad297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996464"
---
# <span data-ttu-id="842a9-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="842a9-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="842a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="842a9-102">SYNOPSIS</span></span>
<span data-ttu-id="842a9-103">애플리케이션 게이트웨이에서 ssl 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="842a9-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="842a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="842a9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="842a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="842a9-105">DESCRIPTION</span></span>
<span data-ttu-id="842a9-106">**Remove-AzApplicationGatewaySslProfile** cmdlet은 애플리케이션 게이트웨이에서 ssl 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="842a9-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="842a9-107">예제</span><span class="sxs-lookup"><span data-stu-id="842a9-107">EXAMPLES</span></span>

### <span data-ttu-id="842a9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="842a9-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="842a9-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="842a9-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="842a9-110">두 번째 명령은 SslProfile01이라는 ssl 프로필을 에 저장된 애플리케이션 게이트웨이에서 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="842a9-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="842a9-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="842a9-111">PARAMETERS</span></span>

### <span data-ttu-id="842a9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="842a9-112">-ApplicationGateway</span></span>
<span data-ttu-id="842a9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="842a9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="842a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842a9-114">-DefaultProfile</span></span>
<span data-ttu-id="842a9-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="842a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="842a9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="842a9-116">-Name</span></span>
<span data-ttu-id="842a9-117">ssl 프로필의 이름</span><span class="sxs-lookup"><span data-stu-id="842a9-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="842a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842a9-118">CommonParameters</span></span>
<span data-ttu-id="842a9-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="842a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842a9-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="842a9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842a9-121">입력</span><span class="sxs-lookup"><span data-stu-id="842a9-121">INPUTS</span></span>

### <span data-ttu-id="842a9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="842a9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="842a9-123">출력</span><span class="sxs-lookup"><span data-stu-id="842a9-123">OUTPUTS</span></span>

### <span data-ttu-id="842a9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="842a9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="842a9-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="842a9-125">NOTES</span></span>

## <span data-ttu-id="842a9-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="842a9-126">RELATED LINKS</span></span>

[<span data-ttu-id="842a9-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="842a9-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="842a9-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="842a9-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="842a9-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="842a9-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="842a9-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="842a9-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)