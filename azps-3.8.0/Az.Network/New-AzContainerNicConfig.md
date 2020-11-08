---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 75f05c76b76f37e936798766d9288ace38d1397f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044758"
---
# <span data-ttu-id="18a53-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="18a53-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="18a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18a53-102">SYNOPSIS</span></span>
<span data-ttu-id="18a53-103">새 컨테이너 네트워크 인터페이스 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="18a53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18a53-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18a53-105">DESCRIPTION</span></span>
<span data-ttu-id="18a53-106">**AzContainerNicConfig** cmdlet은 새 컨테이너 네트워크 인터페이스 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="18a53-107">이 개체는 상위 네트워크 프로필을 참조 하 여 만든 컨테이너 네트워크 인터페이스의 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="18a53-108">예제의</span><span class="sxs-lookup"><span data-stu-id="18a53-108">EXAMPLES</span></span>

### <span data-ttu-id="18a53-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="18a53-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="18a53-110">첫 번째 명령은 빈 컨테이너 네트워크 인터페이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="18a53-111">두 번째는 이전에 생성 된 컨테이너 네트워크 인터페이스 구성을 New-NetworkProfile cmdlet에 인수로 전달 하 여 새 네트워크 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="18a53-112">변수</span><span class="sxs-lookup"><span data-stu-id="18a53-112">PARAMETERS</span></span>

### <span data-ttu-id="18a53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a53-113">-DefaultProfile</span></span>
<span data-ttu-id="18a53-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a53-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18a53-115">-IpConfiguration</span></span>
<span data-ttu-id="18a53-116">컨테이너 nic를이 컨테이너 네트워크 인터페이스 구성에서 인스턴스화할 때 만들어지는 ip 구성을 결정 하는 IP 구성 프로필 모음</span><span class="sxs-lookup"><span data-stu-id="18a53-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a53-117">-이름</span><span class="sxs-lookup"><span data-stu-id="18a53-117">-Name</span></span>
<span data-ttu-id="18a53-118">컨테이너 네트워크 인터페이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="18a53-119">-확인</span><span class="sxs-lookup"><span data-stu-id="18a53-119">-Confirm</span></span>
<span data-ttu-id="18a53-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a53-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a53-121">-WhatIf</span></span>
<span data-ttu-id="18a53-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a53-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a53-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a53-124">CommonParameters</span></span>
<span data-ttu-id="18a53-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18a53-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a53-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18a53-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a53-127">입력</span><span class="sxs-lookup"><span data-stu-id="18a53-127">INPUTS</span></span>

### <span data-ttu-id="18a53-128">PSIPConfigurationProfile [] (으)로</span><span class="sxs-lookup"><span data-stu-id="18a53-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="18a53-129">출력</span><span class="sxs-lookup"><span data-stu-id="18a53-129">OUTPUTS</span></span>

### <span data-ttu-id="18a53-130">PSContainerNetworkInterfaceConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="18a53-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="18a53-131">상속자</span><span class="sxs-lookup"><span data-stu-id="18a53-131">NOTES</span></span>

## <span data-ttu-id="18a53-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18a53-132">RELATED LINKS</span></span>

[<span data-ttu-id="18a53-133">새로운 AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="18a53-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
