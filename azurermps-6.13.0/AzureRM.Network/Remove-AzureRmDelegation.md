---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711056"
---
# <span data-ttu-id="a1b26-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a1b26-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="a1b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b26-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b26-103">제공 된 서브넷에서 서비스 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1b26-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a1b26-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b26-106">**AzureRmDelegation** cmdlet은 위임을 사용 하 여 서브넷을 가져와 해당 서브넷에서 명명 된 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="a1b26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a1b26-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b26-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a1b26-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="a1b26-109">이 예제에서 첫 번째 절반 ( _"기존 서브넷에 대 한 위임 추가"_ 아래에 있음)은 [Add-AzureRmDelegation](./Add-AzureRmDelegation.md)와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="a1b26-110">두 번째 부분에서는 첫 번째 두 cmdlet이 원하는 서브넷을 검색 하 고 서버에 있는 항목을 사용 하 여 로컬 복사본을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="a1b26-111">세 번째 cmdlet은 _Mysubnet_ 의 첫 절반에서 만들어진 위임을 제거 하 고 _$subnet_ 에 업데이트 된 서브넷을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="a1b26-112">최종 cmdlet은 제거 된 위임을 사용 하 여 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="a1b26-113">변수</span><span class="sxs-lookup"><span data-stu-id="a1b26-113">PARAMETERS</span></span>

### <span data-ttu-id="a1b26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b26-114">-DefaultProfile</span></span>
<span data-ttu-id="a1b26-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b26-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a1b26-116">-Name</span></span>
<span data-ttu-id="a1b26-117">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b26-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a1b26-118">-ServiceName</span></span>
<span data-ttu-id="a1b26-119">서브넷을 위임할 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="a1b26-120">-서브넷</span><span class="sxs-lookup"><span data-stu-id="a1b26-120">-Subnet</span></span>
<span data-ttu-id="a1b26-121">위임을 제거할 서브넷</span><span class="sxs-lookup"><span data-stu-id="a1b26-121">The subnet from which to remove the delegation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b26-122">CommonParameters</span></span>
<span data-ttu-id="a1b26-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b26-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b26-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b26-125">입력</span><span class="sxs-lookup"><span data-stu-id="a1b26-125">INPUTS</span></span>

### <span data-ttu-id="a1b26-126">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a1b26-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="a1b26-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1b26-127">System.String</span></span>
## <span data-ttu-id="a1b26-128">출력</span><span class="sxs-lookup"><span data-stu-id="a1b26-128">OUTPUTS</span></span>

### <span data-ttu-id="a1b26-129">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a1b26-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="a1b26-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a1b26-130">NOTES</span></span>

## <span data-ttu-id="a1b26-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1b26-131">RELATED LINKS</span></span>

<span data-ttu-id="a1b26-132">[추가-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [새로운 AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="a1b26-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
