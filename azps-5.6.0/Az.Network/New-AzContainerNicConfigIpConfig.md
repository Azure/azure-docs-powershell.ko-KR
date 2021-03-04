---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 6ed82377de2a87b3bc40d3d4e8dff6af751ed1f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958592"
---
# <span data-ttu-id="e28c6-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e28c6-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="e28c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e28c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e28c6-103">컨테이너 nic 구성 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="e28c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="e28c6-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e28c6-105">설명</span><span class="sxs-lookup"><span data-stu-id="e28c6-105">DESCRIPTION</span></span>
<span data-ttu-id="e28c6-106">**New-AzContainerNicConfigIpConfig** cmdlet은 새 컨테이너 네트워크 인터페이스 구성 ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="e28c6-107">예제</span><span class="sxs-lookup"><span data-stu-id="e28c6-107">EXAMPLES</span></span>

### <span data-ttu-id="e28c6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e28c6-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="e28c6-109">처음 두 명령은 vnet 및 서브넷을 만들고 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="e28c6-110">세 번째 명령은 만든 서브넷을 참조하는 컨테이너 nic ip 구성 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="e28c6-111">네 번째 명령은 이전 명령에서 만든 IP 구성 프로필을 공급하는 컨테이너 네트워크 인터페이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="e28c6-112">마지막으로, 다섯 번째 명령은 컨테이너 네트워크 인터페이스 구성으로 초기화된 네트워크 프로필을 $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="e28c6-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="e28c6-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e28c6-113">PARAMETERS</span></span>

### <span data-ttu-id="e28c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28c6-114">-DefaultProfile</span></span>
<span data-ttu-id="e28c6-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e28c6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e28c6-116">-Name</span></span>
<span data-ttu-id="e28c6-117">컨테이너 네트워크 인터페이스 구성 ip 구성 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="e28c6-118">-서브넷</span><span class="sxs-lookup"><span data-stu-id="e28c6-118">-Subnet</span></span>
<span data-ttu-id="e28c6-119">서브넷</span><span class="sxs-lookup"><span data-stu-id="e28c6-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28c6-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e28c6-120">-SubnetId</span></span>
<span data-ttu-id="e28c6-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="e28c6-121">SubnetId</span></span>

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

### <span data-ttu-id="e28c6-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e28c6-122">-Confirm</span></span>
<span data-ttu-id="e28c6-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28c6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e28c6-124">-WhatIf</span></span>
<span data-ttu-id="e28c6-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e28c6-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28c6-127">CommonParameters</span></span>
<span data-ttu-id="e28c6-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e28c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28c6-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e28c6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28c6-130">입력</span><span class="sxs-lookup"><span data-stu-id="e28c6-130">INPUTS</span></span>

### <span data-ttu-id="e28c6-131">없음</span><span class="sxs-lookup"><span data-stu-id="e28c6-131">None</span></span>

## <span data-ttu-id="e28c6-132">출력</span><span class="sxs-lookup"><span data-stu-id="e28c6-132">OUTPUTS</span></span>

### <span data-ttu-id="e28c6-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e28c6-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e28c6-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e28c6-134">NOTES</span></span>

## <span data-ttu-id="e28c6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e28c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="e28c6-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e28c6-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
