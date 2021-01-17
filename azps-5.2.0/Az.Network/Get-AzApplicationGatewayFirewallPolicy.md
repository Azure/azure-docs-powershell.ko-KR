---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359206"
---
# <span data-ttu-id="65b92-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="65b92-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="65b92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b92-102">SYNOPSIS</span></span>
<span data-ttu-id="65b92-103">애플리케이션 게이트웨이 방화벽 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="65b92-104">구문</span><span class="sxs-lookup"><span data-stu-id="65b92-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b92-105">설명</span><span class="sxs-lookup"><span data-stu-id="65b92-105">DESCRIPTION</span></span>
<span data-ttu-id="65b92-106">**Get-AzApplicationGatewayFirewallPolicy** cmdlet은 애플리케이션 게이트웨이 방화벽 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="65b92-107">예제</span><span class="sxs-lookup"><span data-stu-id="65b92-107">EXAMPLES</span></span>

### <span data-ttu-id="65b92-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="65b92-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="65b92-109">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 FirewallPolicy1이라는 애플리케이션 게이트웨이 방화벽 정책을 $AppGwFirewallPolicy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="65b92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65b92-110">PARAMETERS</span></span>

### <span data-ttu-id="65b92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b92-111">-DefaultProfile</span></span>
<span data-ttu-id="65b92-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b92-113">-Name</span><span class="sxs-lookup"><span data-stu-id="65b92-113">-Name</span></span>
<span data-ttu-id="65b92-114">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b92-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b92-115">-ResourceGroupName</span></span>
<span data-ttu-id="65b92-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b92-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b92-117">CommonParameters</span></span>
<span data-ttu-id="65b92-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65b92-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b92-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65b92-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b92-120">입력</span><span class="sxs-lookup"><span data-stu-id="65b92-120">INPUTS</span></span>

### <span data-ttu-id="65b92-121">System.String</span><span class="sxs-lookup"><span data-stu-id="65b92-121">System.String</span></span>

## <span data-ttu-id="65b92-122">출력</span><span class="sxs-lookup"><span data-stu-id="65b92-122">OUTPUTS</span></span>

### <span data-ttu-id="65b92-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="65b92-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="65b92-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65b92-124">NOTES</span></span>

## <span data-ttu-id="65b92-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65b92-125">RELATED LINKS</span></span>
