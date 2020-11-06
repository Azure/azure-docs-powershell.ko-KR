---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: f2e0bb88df867da0a110422debea4d6688ad3af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533955"
---
# <span data-ttu-id="24d48-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="24d48-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="24d48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d48-102">SYNOPSIS</span></span>
<span data-ttu-id="24d48-103">가상 네트워크에서 서브넷 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24d48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24d48-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d48-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24d48-105">DESCRIPTION</span></span>
<span data-ttu-id="24d48-106">**AzureRmVirtualNetworkSubnetConfig** Cmdlet은 Azure 가상 네트워크에서 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="24d48-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24d48-107">EXAMPLES</span></span>

### <span data-ttu-id="24d48-108">1: 가상 네트워크에서 서브넷을 제거 하 고 가상 네트워크 업데이트</span><span class="sxs-lookup"><span data-stu-id="24d48-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="24d48-109">이 예제에서는 두 개의 서브넷이 있는 리소스 그룹과 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="24d48-110">그런 다음 Remove-AzureRmVirtualNetworkSubnetConfig 명령을 사용 하 여 가상 네트워크의 메모리 내 표현에서 백 엔드 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="24d48-111">그런 다음 서버 쪽에서 가상 네트워크를 수정 하기 위해 Set-AzureRmVirtualNetwork 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="24d48-112">변수</span><span class="sxs-lookup"><span data-stu-id="24d48-112">PARAMETERS</span></span>

### <span data-ttu-id="24d48-113">-이름</span><span class="sxs-lookup"><span data-stu-id="24d48-113">-Name</span></span>
<span data-ttu-id="24d48-114">제거할 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-114">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d48-115">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="24d48-115">-VirtualNetwork</span></span>
<span data-ttu-id="24d48-116">제거할 서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-116">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24d48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d48-117">-DefaultProfile</span></span>
<span data-ttu-id="24d48-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d48-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d48-119">CommonParameters</span></span>
<span data-ttu-id="24d48-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d48-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d48-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d48-122">입력</span><span class="sxs-lookup"><span data-stu-id="24d48-122">INPUTS</span></span>

### <span data-ttu-id="24d48-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="24d48-123">PSVirtualNetwork</span></span>
<span data-ttu-id="24d48-124">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d48-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="24d48-125">출력</span><span class="sxs-lookup"><span data-stu-id="24d48-125">OUTPUTS</span></span>

### <span data-ttu-id="24d48-126">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="24d48-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="24d48-127">상속자</span><span class="sxs-lookup"><span data-stu-id="24d48-127">NOTES</span></span>

## <span data-ttu-id="24d48-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24d48-128">RELATED LINKS</span></span>

[<span data-ttu-id="24d48-129">추가-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="24d48-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="24d48-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="24d48-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="24d48-131">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="24d48-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="24d48-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="24d48-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


