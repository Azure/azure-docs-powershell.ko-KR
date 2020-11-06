---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531400"
---
# <span data-ttu-id="b196a-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b196a-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="b196a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b196a-102">SYNOPSIS</span></span>
<span data-ttu-id="b196a-103">컨테이너 nic 구성 ip 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b196a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b196a-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b196a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b196a-105">DESCRIPTION</span></span>
<span data-ttu-id="b196a-106">**AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet은 새 컨테이너 네트워크 인터페이스 구성 ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="b196a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b196a-107">EXAMPLES</span></span>

### <span data-ttu-id="b196a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b196a-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="b196a-109">처음 두 명령은 vnet 및 서브넷을 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="b196a-110">세 번째 명령은 만든 서브넷을 참조 하는 컨테이너 nic ip 구성 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="b196a-111">네 번째 명령은 이전 명령에서 만든 ip 구성 프로필을 제공 하는 컨테이너 네트워크 인터페이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="b196a-112">마지막으로 다섯 번째 명령은 $containerNicConfig에 저장 된 컨테이너 네트워크 인터페이스 구성을 사용 하 여 초기화 된 네트워크 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="b196a-113">변수</span><span class="sxs-lookup"><span data-stu-id="b196a-113">PARAMETERS</span></span>

### <span data-ttu-id="b196a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b196a-114">-DefaultProfile</span></span>
<span data-ttu-id="b196a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b196a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b196a-116">-Name</span></span>
<span data-ttu-id="b196a-117">컨테이너 네트워크 인터페이스 구성 ip 구성 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="b196a-118">-서브넷</span><span class="sxs-lookup"><span data-stu-id="b196a-118">-Subnet</span></span>
<span data-ttu-id="b196a-119">서브넷</span><span class="sxs-lookup"><span data-stu-id="b196a-119">Subnet</span></span>

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

### <span data-ttu-id="b196a-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b196a-120">-SubnetId</span></span>
<span data-ttu-id="b196a-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="b196a-121">SubnetId</span></span>

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

### <span data-ttu-id="b196a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b196a-122">-Confirm</span></span>
<span data-ttu-id="b196a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b196a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b196a-124">-WhatIf</span></span>
<span data-ttu-id="b196a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b196a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b196a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b196a-127">CommonParameters</span></span>
<span data-ttu-id="b196a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b196a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b196a-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b196a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b196a-130">입력</span><span class="sxs-lookup"><span data-stu-id="b196a-130">INPUTS</span></span>

### <span data-ttu-id="b196a-131">않아야</span><span class="sxs-lookup"><span data-stu-id="b196a-131">None</span></span>

## <span data-ttu-id="b196a-132">출력</span><span class="sxs-lookup"><span data-stu-id="b196a-132">OUTPUTS</span></span>

### <span data-ttu-id="b196a-133">PSContainerNetworkInterfaceConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b196a-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="b196a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b196a-134">NOTES</span></span>

## <span data-ttu-id="b196a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b196a-135">RELATED LINKS</span></span>
