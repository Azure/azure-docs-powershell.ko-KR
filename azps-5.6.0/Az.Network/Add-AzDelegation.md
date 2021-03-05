---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 779793bcc3df7ae62cc7ae7cc900ed863e8f4ee8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986771"
---
# <span data-ttu-id="e273c-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="e273c-101">Add-AzDelegation</span></span>

## <span data-ttu-id="e273c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e273c-102">SYNOPSIS</span></span>
<span data-ttu-id="e273c-103">서브넷에 위임이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="e273c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e273c-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e273c-105">설명</span><span class="sxs-lookup"><span data-stu-id="e273c-105">DESCRIPTION</span></span>
<span data-ttu-id="e273c-106">**Add-AzDelegation** cmdlet은 Azure 서브넷에 서비스 위임이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="e273c-107">예제</span><span class="sxs-lookup"><span data-stu-id="e273c-107">EXAMPLES</span></span>

### <span data-ttu-id="e273c-108">예제 1: 위임 추가</span><span class="sxs-lookup"><span data-stu-id="e273c-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="e273c-109">첫 번째 명령은 서브넷이 있는 가상 네트워크를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="e273c-110">두 번째 명령은 관심 있는 서브넷(위임할 서브넷)을 격리합니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="e273c-111">세 번째 명령은 서브넷에 위임이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="e273c-112">이 특정 예제는 이 서브넷에서 인터페이스 엔드포인트를 SQL 설정하려는 경우 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="e273c-113">최종 명령은 업데이트된 서브넷을 서버에 보내서 서브넷을 실제로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="e273c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e273c-114">PARAMETERS</span></span>

### <span data-ttu-id="e273c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e273c-115">-DefaultProfile</span></span>
<span data-ttu-id="e273c-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e273c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e273c-117">-Name</span></span>
<span data-ttu-id="e273c-118">위임의 이름</span><span class="sxs-lookup"><span data-stu-id="e273c-118">The name of the delegation</span></span>

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

### <span data-ttu-id="e273c-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e273c-119">-ServiceName</span></span>
<span data-ttu-id="e273c-120">서브넷을 위임해야 하는 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="e273c-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="e273c-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="e273c-121">-Subnet</span></span>
<span data-ttu-id="e273c-122">서브넷</span><span class="sxs-lookup"><span data-stu-id="e273c-122">The subnet</span></span>

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

### <span data-ttu-id="e273c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e273c-123">CommonParameters</span></span>
<span data-ttu-id="e273c-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e273c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e273c-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e273c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e273c-126">입력</span><span class="sxs-lookup"><span data-stu-id="e273c-126">INPUTS</span></span>

### <span data-ttu-id="e273c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e273c-127">System.String</span></span>

### <span data-ttu-id="e273c-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e273c-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e273c-129">출력</span><span class="sxs-lookup"><span data-stu-id="e273c-129">OUTPUTS</span></span>

### <span data-ttu-id="e273c-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e273c-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e273c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e273c-131">NOTES</span></span>

## <span data-ttu-id="e273c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e273c-132">RELATED LINKS</span></span>

<span data-ttu-id="e273c-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="e273c-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>