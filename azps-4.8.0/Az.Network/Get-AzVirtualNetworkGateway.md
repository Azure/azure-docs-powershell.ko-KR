---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204495"
---
# <span data-ttu-id="e0a2f-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0a2f-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="e0a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a2f-103">가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="e0a2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0a2f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a2f-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="e0a2f-107">**AzVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e0a2f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e0a2f-108">EXAMPLES</span></span>

### <span data-ttu-id="e0a2f-109">예제 1: 가상 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="e0a2f-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="e0a2f-110">리소스 그룹 "myRG" 내에서 이름이 "myGateway1" 인 가상 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="e0a2f-111">예제 2: 가상 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="e0a2f-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="e0a2f-112">리소스 그룹 "Mygateway" 내에서 "myGateway"로 시작 하는 모든 가상 네트워크 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="e0a2f-113">변수</span><span class="sxs-lookup"><span data-stu-id="e0a2f-113">PARAMETERS</span></span>

### <span data-ttu-id="e0a2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a2f-114">-DefaultProfile</span></span>
<span data-ttu-id="e0a2f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0a2f-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e0a2f-116">-Name</span></span>
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

### <span data-ttu-id="e0a2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a2f-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e0a2f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a2f-118">CommonParameters</span></span>
<span data-ttu-id="e0a2f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a2f-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a2f-121">입력</span><span class="sxs-lookup"><span data-stu-id="e0a2f-121">INPUTS</span></span>

### <span data-ttu-id="e0a2f-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0a2f-122">System.String</span></span>

## <span data-ttu-id="e0a2f-123">출력</span><span class="sxs-lookup"><span data-stu-id="e0a2f-123">OUTPUTS</span></span>

### <span data-ttu-id="e0a2f-124">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e0a2f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e0a2f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="e0a2f-125">NOTES</span></span>

## <span data-ttu-id="e0a2f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0a2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="e0a2f-127">새로운 AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0a2f-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0a2f-128">제거-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0a2f-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0a2f-129">다시 설정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0a2f-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0a2f-130">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0a2f-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0a2f-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0a2f-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
