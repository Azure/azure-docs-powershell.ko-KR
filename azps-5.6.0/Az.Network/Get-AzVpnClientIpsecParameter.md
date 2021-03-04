---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006267"
---
# <span data-ttu-id="270fb-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="270fb-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="270fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270fb-102">SYNOPSIS</span></span>
<span data-ttu-id="270fb-103">지점 및 사이트 연결에 대한 Virtual Network Gateway에 설정된 VPN Ipsec 매개 변수를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="270fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="270fb-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="270fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="270fb-105">DESCRIPTION</span></span>
<span data-ttu-id="270fb-106">Virtual Network Gateway는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="270fb-107">**Get-AzVpnClientIpsecParameter** cmdlet은 게이트웨이 이름 및 리소스 그룹 이름을 기반으로 Azure의 게이트웨이에 설정된 vpn ipsec 매개 변수의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="270fb-108">예제</span><span class="sxs-lookup"><span data-stu-id="270fb-108">EXAMPLES</span></span>

### <span data-ttu-id="270fb-109">예제 1: 사이트 연결에 대한 Virtual Network Gateway에 설정된 VPN Ipsec 매개 변수를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="270fb-110">리소스 그룹 "myRG" 내에서 "myGateway"라는 이름으로 Virtual Network Gateway에 설정된 vpn ipsec 매개 변수의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="270fb-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="270fb-111">PARAMETERS</span></span>

### <span data-ttu-id="270fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270fb-112">-DefaultProfile</span></span>
<span data-ttu-id="270fb-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="270fb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="270fb-114">-Name</span></span>
<span data-ttu-id="270fb-115">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-115">The resource name.</span></span>

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

### <span data-ttu-id="270fb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270fb-116">-ResourceGroupName</span></span>
<span data-ttu-id="270fb-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270fb-118">CommonParameters</span></span>
<span data-ttu-id="270fb-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="270fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270fb-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="270fb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270fb-121">입력</span><span class="sxs-lookup"><span data-stu-id="270fb-121">INPUTS</span></span>

### <span data-ttu-id="270fb-122">System.String</span><span class="sxs-lookup"><span data-stu-id="270fb-122">System.String</span></span>

## <span data-ttu-id="270fb-123">출력</span><span class="sxs-lookup"><span data-stu-id="270fb-123">OUTPUTS</span></span>

### <span data-ttu-id="270fb-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="270fb-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="270fb-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="270fb-125">NOTES</span></span>

## <span data-ttu-id="270fb-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="270fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="270fb-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="270fb-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="270fb-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="270fb-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="270fb-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="270fb-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
