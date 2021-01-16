---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356085"
---
# <span data-ttu-id="ae378-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ae378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae378-102">SYNOPSIS</span></span>
<span data-ttu-id="ae378-103">Virtual Network 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="ae378-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae378-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae378-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae378-105">DESCRIPTION</span></span>
<span data-ttu-id="ae378-106">Virtual Network 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="ae378-107">**Get-AzVirtualNetworkGateway** cmdlet은 이름 및 리소스 그룹 이름을 기반으로 Azure에서 게이트웨이의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ae378-108">예제</span><span class="sxs-lookup"><span data-stu-id="ae378-108">EXAMPLES</span></span>

### <span data-ttu-id="ae378-109">예제 1: Virtual Network 게이트웨이를 얻게</span><span class="sxs-lookup"><span data-stu-id="ae378-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="ae378-110">리소스 그룹 "myRG" 내에서 이름이 "myGateway1"인 Virtual Network 게이트웨이의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="ae378-111">예제 2: Virtual Network 게이트웨이를 얻게</span><span class="sxs-lookup"><span data-stu-id="ae378-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="ae378-112">리소스 그룹 "myRG" 내에서 "myGateway"로 시작하는 모든 Virtual Network 게이트웨이를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="ae378-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae378-113">PARAMETERS</span></span>

### <span data-ttu-id="ae378-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae378-114">-DefaultProfile</span></span>
<span data-ttu-id="ae378-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae378-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ae378-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae378-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae378-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae378-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae378-118">CommonParameters</span></span>
<span data-ttu-id="ae378-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae378-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae378-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae378-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae378-121">입력</span><span class="sxs-lookup"><span data-stu-id="ae378-121">INPUTS</span></span>

### <span data-ttu-id="ae378-122">System.String</span><span class="sxs-lookup"><span data-stu-id="ae378-122">System.String</span></span>

## <span data-ttu-id="ae378-123">출력</span><span class="sxs-lookup"><span data-stu-id="ae378-123">OUTPUTS</span></span>

### <span data-ttu-id="ae378-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ae378-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae378-125">NOTES</span></span>

## <span data-ttu-id="ae378-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae378-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae378-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ae378-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ae378-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ae378-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ae378-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae378-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
