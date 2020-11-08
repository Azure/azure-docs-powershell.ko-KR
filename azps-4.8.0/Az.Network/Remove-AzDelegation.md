---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048878"
---
# <span data-ttu-id="c6c99-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="c6c99-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="c6c99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c99-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c99-103">제공 된 서브넷에서 서비스 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="c6c99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6c99-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6c99-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6c99-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c99-106">**AzDelegation** cmdlet은 위임을 사용 하 여 서브넷을 가져와 해당 서브넷에서 명명 된 위임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="c6c99-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6c99-107">EXAMPLES</span></span>

### <span data-ttu-id="c6c99-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6c99-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="c6c99-109">이 예제에서 첫 번째 절반 ( _"기존 서브넷에 대 한 위임 추가"_ 아래에 있음)은 [Add-AzDelegation](./Add-AzDelegation.md)와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="c6c99-110">두 번째 부분에서는 첫 번째 두 cmdlet이 원하는 서브넷을 검색 하 고 서버에 있는 항목을 사용 하 여 로컬 복사본을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="c6c99-111">세 번째 cmdlet은 _Mysubnet_ 의 첫 절반에서 만들어진 위임을 제거 하 고 _$subnet_ 에 업데이트 된 서브넷을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="c6c99-112">최종 cmdlet은 제거 된 위임을 사용 하 여 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="c6c99-113">변수</span><span class="sxs-lookup"><span data-stu-id="c6c99-113">PARAMETERS</span></span>

### <span data-ttu-id="c6c99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c99-114">-DefaultProfile</span></span>
<span data-ttu-id="c6c99-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c99-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c6c99-116">-Name</span></span>
<span data-ttu-id="c6c99-117">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-117">The name of the delegation</span></span>

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

### <span data-ttu-id="c6c99-118">-서브넷</span><span class="sxs-lookup"><span data-stu-id="c6c99-118">-Subnet</span></span>
<span data-ttu-id="c6c99-119">위임을 제거할 서브넷</span><span class="sxs-lookup"><span data-stu-id="c6c99-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="c6c99-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c99-120">CommonParameters</span></span>
<span data-ttu-id="c6c99-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c99-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c99-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c99-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c99-123">입력</span><span class="sxs-lookup"><span data-stu-id="c6c99-123">INPUTS</span></span>

### <span data-ttu-id="c6c99-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6c99-124">System.String</span></span>

### <span data-ttu-id="c6c99-125">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c6c99-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c6c99-126">출력</span><span class="sxs-lookup"><span data-stu-id="c6c99-126">OUTPUTS</span></span>

### <span data-ttu-id="c6c99-127">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c6c99-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c6c99-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c6c99-128">NOTES</span></span>

## <span data-ttu-id="c6c99-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6c99-129">RELATED LINKS</span></span>

<span data-ttu-id="c6c99-130">[추가-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [새로운 AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="c6c99-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>