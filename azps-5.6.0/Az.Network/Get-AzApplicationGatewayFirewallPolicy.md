---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 122e011336b9fcdb8b8eb19622632e1ff295a01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996557"
---
# <span data-ttu-id="0fe37-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0fe37-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="0fe37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe37-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe37-103">애플리케이션 게이트웨이 방화벽 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="0fe37-104">구문</span><span class="sxs-lookup"><span data-stu-id="0fe37-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe37-105">설명</span><span class="sxs-lookup"><span data-stu-id="0fe37-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe37-106">**Get-AzApplicationGatewayFirewallPolicy** cmdlet은 애플리케이션 게이트웨이 방화벽 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="0fe37-107">예제</span><span class="sxs-lookup"><span data-stu-id="0fe37-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe37-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0fe37-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0fe37-109">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 FirewallPolicy1이라는 애플리케이션 게이트웨이 방화벽 정책을 $AppGwFirewallPolicy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="0fe37-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0fe37-110">PARAMETERS</span></span>

### <span data-ttu-id="0fe37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe37-111">-DefaultProfile</span></span>
<span data-ttu-id="0fe37-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe37-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0fe37-113">-Name</span></span>
<span data-ttu-id="0fe37-114">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-114">The resource name.</span></span>

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

### <span data-ttu-id="0fe37-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe37-115">-ResourceGroupName</span></span>
<span data-ttu-id="0fe37-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-116">The resource group name.</span></span>

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

### <span data-ttu-id="0fe37-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe37-117">CommonParameters</span></span>
<span data-ttu-id="0fe37-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe37-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe37-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fe37-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe37-120">입력</span><span class="sxs-lookup"><span data-stu-id="0fe37-120">INPUTS</span></span>

### <span data-ttu-id="0fe37-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0fe37-121">System.String</span></span>

## <span data-ttu-id="0fe37-122">출력</span><span class="sxs-lookup"><span data-stu-id="0fe37-122">OUTPUTS</span></span>

### <span data-ttu-id="0fe37-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0fe37-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="0fe37-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0fe37-124">NOTES</span></span>

## <span data-ttu-id="0fe37-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fe37-125">RELATED LINKS</span></span>
