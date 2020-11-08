---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056642"
---
# <span data-ttu-id="eaa0a-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eaa0a-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="eaa0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaa0a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa0a-103">사이트 연결을 위한 가상 네트워크 게이트웨이에 설정 된 vpn Ipsec 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="eaa0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eaa0a-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa0a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eaa0a-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa0a-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="eaa0a-107">**AzVpnClientIpsecParameter** Cmdlet은 게이트웨이 이름 및 리소스 그룹 이름에 기반 하 여 Azure의 게이트웨이에서 설정 된 vpn ipsec 매개 변수 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="eaa0a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="eaa0a-108">EXAMPLES</span></span>

### <span data-ttu-id="eaa0a-109">예제 1: 사이트 간 연결에 대 한 가상 네트워크 게이트웨이에 설정 된 vpn Ipsec 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="eaa0a-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이에 설정 된 vpn ipsec 매개 변수 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="eaa0a-111">변수</span><span class="sxs-lookup"><span data-stu-id="eaa0a-111">PARAMETERS</span></span>

### <span data-ttu-id="eaa0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa0a-112">-DefaultProfile</span></span>
<span data-ttu-id="eaa0a-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaa0a-114">-이름</span><span class="sxs-lookup"><span data-stu-id="eaa0a-114">-Name</span></span>
<span data-ttu-id="eaa0a-115">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-115">The resource name.</span></span>

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

### <span data-ttu-id="eaa0a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa0a-116">-ResourceGroupName</span></span>
<span data-ttu-id="eaa0a-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-117">The resource group name.</span></span>

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

### <span data-ttu-id="eaa0a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa0a-118">CommonParameters</span></span>
<span data-ttu-id="eaa0a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa0a-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa0a-121">입력</span><span class="sxs-lookup"><span data-stu-id="eaa0a-121">INPUTS</span></span>

### <span data-ttu-id="eaa0a-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eaa0a-122">System.String</span></span>

## <span data-ttu-id="eaa0a-123">출력</span><span class="sxs-lookup"><span data-stu-id="eaa0a-123">OUTPUTS</span></span>

### <span data-ttu-id="eaa0a-124">PSVpnClientIPsecParameters에 대 한.</span><span class="sxs-lookup"><span data-stu-id="eaa0a-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="eaa0a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="eaa0a-125">NOTES</span></span>

## <span data-ttu-id="eaa0a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eaa0a-126">RELATED LINKS</span></span>

[<span data-ttu-id="eaa0a-127">새로운 AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eaa0a-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="eaa0a-128">제거-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eaa0a-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="eaa0a-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eaa0a-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
