---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 9ce01263acde5b30533a23d55a8e7cedaba6b53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870078"
---
# <span data-ttu-id="5bd19-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5bd19-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5bd19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd19-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd19-103">가상 네트워크 게이트웨이 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="5bd19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5bd19-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bd19-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5bd19-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd19-106">가상 네트워크 게이트웨이 연결은 Azure의 가상 네트워크 게이트웨이에 연결 된 IPsec 터널 (사이트 간 또는 Vnet to Vnet)을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="5bd19-107">**AzVirtualNetworkGatewayConnection** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 연결 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="5bd19-108">-Name 매개 변수를 지정 하지 않고 **AzVirtualNetworkGatewayConnection** cmdlet을 실행 하는 경우 출력에 Connectionstatus 및 sharedkey 정보가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="5bd19-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5bd19-109">EXAMPLES</span></span>

### <span data-ttu-id="5bd19-110">1: 가상 네트워크 게이트웨이 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="5bd19-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="5bd19-111">리소스 그룹 "Mytunnel" 내에서 이름이 "myTunnel" 인 가상 네트워크 게이트웨이 연결의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="5bd19-112">2: 필터링을 사용 하 여 모든 가상 네트워크 게이트웨이 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="5bd19-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="5bd19-113">리소스 그룹 "Mytunnel" 내에서 "myTunnel"로 시작 하는 모든 가상 네트워크 게이트웨이 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="5bd19-114">변수</span><span class="sxs-lookup"><span data-stu-id="5bd19-114">PARAMETERS</span></span>

### <span data-ttu-id="5bd19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd19-115">-DefaultProfile</span></span>
<span data-ttu-id="5bd19-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bd19-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5bd19-117">-Name</span></span>
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

### <span data-ttu-id="5bd19-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd19-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5bd19-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd19-119">CommonParameters</span></span>
<span data-ttu-id="5bd19-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd19-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd19-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bd19-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd19-122">입력</span><span class="sxs-lookup"><span data-stu-id="5bd19-122">INPUTS</span></span>

### <span data-ttu-id="5bd19-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5bd19-123">System.String</span></span>

## <span data-ttu-id="5bd19-124">출력</span><span class="sxs-lookup"><span data-stu-id="5bd19-124">OUTPUTS</span></span>

### <span data-ttu-id="5bd19-125">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5bd19-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5bd19-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5bd19-126">NOTES</span></span>

## <span data-ttu-id="5bd19-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bd19-127">RELATED LINKS</span></span>

[<span data-ttu-id="5bd19-128">새로운 AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5bd19-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5bd19-129">제거-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5bd19-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5bd19-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5bd19-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
