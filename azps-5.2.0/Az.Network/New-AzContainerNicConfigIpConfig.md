---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369307"
---
# <span data-ttu-id="71e3e-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="71e3e-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="71e3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="71e3e-103">컨테이너 nic 구성 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="71e3e-104">구문</span><span class="sxs-lookup"><span data-stu-id="71e3e-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e3e-105">설명</span><span class="sxs-lookup"><span data-stu-id="71e3e-105">DESCRIPTION</span></span>
<span data-ttu-id="71e3e-106">**New-AzContainerNicConfigIpConfig** cmdlet은 새 컨테이너 네트워크 인터페이스 구성 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="71e3e-107">예제</span><span class="sxs-lookup"><span data-stu-id="71e3e-107">EXAMPLES</span></span>

### <span data-ttu-id="71e3e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="71e3e-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="71e3e-109">처음 두 명령은 vnet 및 서브넷을 만들고 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="71e3e-110">세 번째 명령은 만든 서브넷을 참조하는 컨테이너 nic IP 구성 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="71e3e-111">네 번째 명령은 이전 명령에서 만든 IP 구성 프로필을 공급하는 컨테이너 네트워크 인터페이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="71e3e-112">마지막으로, 다섯 번째 명령은 컨테이너 네트워크 인터페이스 구성을 사용하여 초기화된 네트워크 프로필을 $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="71e3e-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="71e3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e3e-113">PARAMETERS</span></span>

### <span data-ttu-id="71e3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e3e-114">-DefaultProfile</span></span>
<span data-ttu-id="71e3e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e3e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="71e3e-116">-Name</span></span>
<span data-ttu-id="71e3e-117">컨테이너 네트워크 인터페이스 구성 IP 구성 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="71e3e-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="71e3e-118">-Subnet</span></span>
<span data-ttu-id="71e3e-119">서브넷</span><span class="sxs-lookup"><span data-stu-id="71e3e-119">Subnet</span></span>

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

### <span data-ttu-id="71e3e-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="71e3e-120">-SubnetId</span></span>
<span data-ttu-id="71e3e-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="71e3e-121">SubnetId</span></span>

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

### <span data-ttu-id="71e3e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71e3e-122">-Confirm</span></span>
<span data-ttu-id="71e3e-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e3e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e3e-124">-WhatIf</span></span>
<span data-ttu-id="71e3e-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71e3e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e3e-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e3e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e3e-127">CommonParameters</span></span>
<span data-ttu-id="71e3e-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71e3e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e3e-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="71e3e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e3e-130">입력</span><span class="sxs-lookup"><span data-stu-id="71e3e-130">INPUTS</span></span>

### <span data-ttu-id="71e3e-131">없음</span><span class="sxs-lookup"><span data-stu-id="71e3e-131">None</span></span>

## <span data-ttu-id="71e3e-132">출력</span><span class="sxs-lookup"><span data-stu-id="71e3e-132">OUTPUTS</span></span>

### <span data-ttu-id="71e3e-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="71e3e-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="71e3e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71e3e-134">NOTES</span></span>

## <span data-ttu-id="71e3e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71e3e-135">RELATED LINKS</span></span>

[<span data-ttu-id="71e3e-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="71e3e-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
