---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218550"
---
# <span data-ttu-id="f7db8-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7db8-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="f7db8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7db8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7db8-103">컨테이너 nic 구성 ip 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="f7db8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7db8-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7db8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f7db8-105">DESCRIPTION</span></span>
<span data-ttu-id="f7db8-106">**AzContainerNicConfigIpConfig** cmdlet은 새 컨테이너 네트워크 인터페이스 구성 ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="f7db8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f7db8-107">EXAMPLES</span></span>

### <span data-ttu-id="f7db8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7db8-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="f7db8-109">처음 두 명령은 vnet 및 서브넷을 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="f7db8-110">세 번째 명령은 만든 서브넷을 참조 하는 컨테이너 nic ip 구성 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="f7db8-111">네 번째 명령은 이전 명령에서 만든 ip 구성 프로필을 제공 하는 컨테이너 네트워크 인터페이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="f7db8-112">마지막으로 다섯 번째 명령은 $containerNicConfig에 저장 된 컨테이너 네트워크 인터페이스 구성을 사용 하 여 초기화 된 네트워크 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="f7db8-113">변수</span><span class="sxs-lookup"><span data-stu-id="f7db8-113">PARAMETERS</span></span>

### <span data-ttu-id="f7db8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7db8-114">-DefaultProfile</span></span>
<span data-ttu-id="f7db8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7db8-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f7db8-116">-Name</span></span>
<span data-ttu-id="f7db8-117">컨테이너 네트워크 인터페이스 구성 ip 구성 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="f7db8-118">-서브넷</span><span class="sxs-lookup"><span data-stu-id="f7db8-118">-Subnet</span></span>
<span data-ttu-id="f7db8-119">서브넷</span><span class="sxs-lookup"><span data-stu-id="f7db8-119">Subnet</span></span>

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

### <span data-ttu-id="f7db8-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f7db8-120">-SubnetId</span></span>
<span data-ttu-id="f7db8-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="f7db8-121">SubnetId</span></span>

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

### <span data-ttu-id="f7db8-122">-확인</span><span class="sxs-lookup"><span data-stu-id="f7db8-122">-Confirm</span></span>
<span data-ttu-id="f7db8-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7db8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7db8-124">-WhatIf</span></span>
<span data-ttu-id="f7db8-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7db8-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7db8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7db8-127">CommonParameters</span></span>
<span data-ttu-id="f7db8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7db8-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7db8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7db8-130">입력</span><span class="sxs-lookup"><span data-stu-id="f7db8-130">INPUTS</span></span>

### <span data-ttu-id="f7db8-131">않아야</span><span class="sxs-lookup"><span data-stu-id="f7db8-131">None</span></span>

## <span data-ttu-id="f7db8-132">출력</span><span class="sxs-lookup"><span data-stu-id="f7db8-132">OUTPUTS</span></span>

### <span data-ttu-id="f7db8-133">PSContainerNetworkInterfaceConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f7db8-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="f7db8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f7db8-134">NOTES</span></span>

## <span data-ttu-id="f7db8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7db8-135">RELATED LINKS</span></span>

[<span data-ttu-id="f7db8-136">새로운 AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f7db8-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
