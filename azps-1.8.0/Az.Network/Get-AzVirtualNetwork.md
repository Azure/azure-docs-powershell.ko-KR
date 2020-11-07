---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: da0dde546d5875c1a29bd02805f40c7f12a68188
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700488"
---
# <span data-ttu-id="7e0d2-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e0d2-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="7e0d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0d2-103">리소스 그룹의 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="7e0d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e0d2-104">SYNTAX</span></span>

### <span data-ttu-id="7e0d2-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="7e0d2-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e0d2-106">확장</span><span class="sxs-lookup"><span data-stu-id="7e0d2-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0d2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7e0d2-107">DESCRIPTION</span></span>
<span data-ttu-id="7e0d2-108">**AzVirtualNetwork** cmdlet은 하나 이상의 가상 네트워크 n 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="7e0d2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7e0d2-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0d2-110">1: 가상 네트워크 검색</span><span class="sxs-lookup"><span data-stu-id="7e0d2-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="7e0d2-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyVirtualNetwork 이라는 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="7e0d2-112">2: 필터를 사용 하 여 가상 네트워크 나열</span><span class="sxs-lookup"><span data-stu-id="7e0d2-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="7e0d2-113">이 명령은 "MyVirtualNetwork"로 시작 하는 모든 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="7e0d2-114">변수</span><span class="sxs-lookup"><span data-stu-id="7e0d2-114">PARAMETERS</span></span>

### <span data-ttu-id="7e0d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0d2-115">-DefaultProfile</span></span>
<span data-ttu-id="7e0d2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e0d2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7e0d2-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0d2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7e0d2-118">-Name</span></span>
<span data-ttu-id="7e0d2-119">이 cmdlet이 가져오는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7e0d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e0d2-121">가상 네트워크가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7e0d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0d2-122">CommonParameters</span></span>
<span data-ttu-id="7e0d2-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0d2-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0d2-125">입력</span><span class="sxs-lookup"><span data-stu-id="7e0d2-125">INPUTS</span></span>

### <span data-ttu-id="7e0d2-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e0d2-126">System.String</span></span>

## <span data-ttu-id="7e0d2-127">출력</span><span class="sxs-lookup"><span data-stu-id="7e0d2-127">OUTPUTS</span></span>

### <span data-ttu-id="7e0d2-128">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7e0d2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7e0d2-129">NOTES</span></span>

## <span data-ttu-id="7e0d2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e0d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="7e0d2-131">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e0d2-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7e0d2-132">제거-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e0d2-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="7e0d2-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e0d2-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


