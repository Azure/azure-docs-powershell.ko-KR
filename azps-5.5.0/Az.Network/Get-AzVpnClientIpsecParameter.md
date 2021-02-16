---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191916"
---
# <span data-ttu-id="91832-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="91832-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="91832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91832-102">SYNOPSIS</span></span>
<span data-ttu-id="91832-103">지점 및 사이트 연결에 대한 Virtual Network Gateway에 설정된 vpn Ipsec 매개 변수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="91832-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="91832-104">구문</span><span class="sxs-lookup"><span data-stu-id="91832-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91832-105">설명</span><span class="sxs-lookup"><span data-stu-id="91832-105">DESCRIPTION</span></span>
<span data-ttu-id="91832-106">Virtual Network 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="91832-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="91832-107">**Get-AzVpnClientIpsecParameter** cmdlet은 게이트웨이 이름 및 리소스 그룹 이름에 따라 Azure의 게이트웨이에 설정된 vpn ipsec 매개 변수의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91832-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="91832-108">예제</span><span class="sxs-lookup"><span data-stu-id="91832-108">EXAMPLES</span></span>

### <span data-ttu-id="91832-109">예제 1: 지점 및 사이트 연결에 대한 Virtual Network Gateway에 설정된 vpn Ipsec 매개 변수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="91832-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="91832-110">리소스 그룹 "myRG" 내에서 "myGateway"라는 이름으로 Virtual Network Gateway에 설정된 vpn ipsec 매개 변수의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91832-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="91832-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91832-111">PARAMETERS</span></span>

### <span data-ttu-id="91832-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91832-112">-DefaultProfile</span></span>
<span data-ttu-id="91832-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91832-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91832-114">-Name</span><span class="sxs-lookup"><span data-stu-id="91832-114">-Name</span></span>
<span data-ttu-id="91832-115">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91832-115">The resource name.</span></span>

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

### <span data-ttu-id="91832-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91832-116">-ResourceGroupName</span></span>
<span data-ttu-id="91832-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91832-117">The resource group name.</span></span>

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

### <span data-ttu-id="91832-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91832-118">CommonParameters</span></span>
<span data-ttu-id="91832-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91832-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91832-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91832-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91832-121">입력</span><span class="sxs-lookup"><span data-stu-id="91832-121">INPUTS</span></span>

### <span data-ttu-id="91832-122">System.String</span><span class="sxs-lookup"><span data-stu-id="91832-122">System.String</span></span>

## <span data-ttu-id="91832-123">출력</span><span class="sxs-lookup"><span data-stu-id="91832-123">OUTPUTS</span></span>

### <span data-ttu-id="91832-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="91832-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="91832-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91832-125">NOTES</span></span>

## <span data-ttu-id="91832-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91832-126">RELATED LINKS</span></span>

[<span data-ttu-id="91832-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="91832-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="91832-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="91832-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="91832-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="91832-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
