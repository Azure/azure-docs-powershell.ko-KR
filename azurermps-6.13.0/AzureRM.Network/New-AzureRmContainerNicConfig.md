---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711648"
---
# <span data-ttu-id="a8002-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a8002-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="a8002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8002-102">SYNOPSIS</span></span>
<span data-ttu-id="a8002-103">새 컨테이너 네트워크 인터페이스 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8002-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8002-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8002-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8002-105">DESCRIPTION</span></span>
<span data-ttu-id="a8002-106">**AzureRmNetworkProfileContainerNicConfig** cmdlet은 새 컨테이너 네트워크 인터페이스 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="a8002-107">이 개체는 상위 네트워크 프로필을 참조 하 여 만들어진 컨테이너 네트워크 interfacs의 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="a8002-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a8002-108">EXAMPLES</span></span>

### <span data-ttu-id="a8002-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8002-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="a8002-110">첫 번째 명령은 빈 컨테이너 네트워크 인터페이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="a8002-111">두 번째는 이전에 생성 된 컨테이너 네트워크 인터페이스 구성을 New-NetworkProfile cmdlet에 인수로 전달 하 여 새 네트워크 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="a8002-112">변수</span><span class="sxs-lookup"><span data-stu-id="a8002-112">PARAMETERS</span></span>

### <span data-ttu-id="a8002-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8002-113">-DefaultProfile</span></span>
<span data-ttu-id="a8002-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8002-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8002-115">-IpConfiguration</span></span>
<span data-ttu-id="a8002-116">{{IpConfiguration 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="a8002-116">{{Fill IpConfiguration Description}}</span></span>

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

### <span data-ttu-id="a8002-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a8002-117">-Name</span></span>
<span data-ttu-id="a8002-118">컨테이너 네트워크 인터페이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="a8002-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a8002-119">-Confirm</span></span>
<span data-ttu-id="a8002-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8002-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8002-121">-WhatIf</span></span>
<span data-ttu-id="a8002-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8002-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8002-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8002-124">CommonParameters</span></span>
<span data-ttu-id="a8002-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8002-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8002-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8002-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8002-127">입력</span><span class="sxs-lookup"><span data-stu-id="a8002-127">INPUTS</span></span>

### <span data-ttu-id="a8002-128">System.webserver. List ' 1 [[PSIPConfigurationProfile, Microsoft azure. 6.7.0.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a8002-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a8002-129">출력</span><span class="sxs-lookup"><span data-stu-id="a8002-129">OUTPUTS</span></span>

### <span data-ttu-id="a8002-130">PSContainerNetworkInterfaceConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a8002-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="a8002-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a8002-131">NOTES</span></span>

## <span data-ttu-id="a8002-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8002-132">RELATED LINKS</span></span>
