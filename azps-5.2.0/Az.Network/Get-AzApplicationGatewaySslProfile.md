---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337869"
---
# <span data-ttu-id="a32a9-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a32a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a32a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a32a9-103">애플리케이션 게이트웨이의 SSL 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a32a9-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="a32a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a32a9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a32a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="a32a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a32a9-106">**Get-AzApplicationGatewaySslProfile** cmdlet은 애플리케이션 게이트웨이의 SSL 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a32a9-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="a32a9-107">예제</span><span class="sxs-lookup"><span data-stu-id="a32a9-107">EXAMPLES</span></span>

### <span data-ttu-id="a32a9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a32a9-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a32a9-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 SSL 프로필 SslProfile01을 $AppGw 변수에 $profile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a32a9-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="a32a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a32a9-110">PARAMETERS</span></span>

### <span data-ttu-id="a32a9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a32a9-111">-ApplicationGateway</span></span>
<span data-ttu-id="a32a9-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a32a9-112">The applicationGateway</span></span>

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

### <span data-ttu-id="a32a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-113">-DefaultProfile</span></span>
<span data-ttu-id="a32a9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a32a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a32a9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a32a9-115">-Name</span></span>
<span data-ttu-id="a32a9-116">ssl 프로필의 이름</span><span class="sxs-lookup"><span data-stu-id="a32a9-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="a32a9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32a9-117">CommonParameters</span></span>
<span data-ttu-id="a32a9-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a32a9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32a9-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a32a9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32a9-120">입력</span><span class="sxs-lookup"><span data-stu-id="a32a9-120">INPUTS</span></span>

### <span data-ttu-id="a32a9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a32a9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a32a9-122">출력</span><span class="sxs-lookup"><span data-stu-id="a32a9-122">OUTPUTS</span></span>

### <span data-ttu-id="a32a9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a32a9-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a32a9-124">NOTES</span></span>

## <span data-ttu-id="a32a9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a32a9-125">RELATED LINKS</span></span>

[<span data-ttu-id="a32a9-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="a32a9-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="a32a9-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="a32a9-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a32a9-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)