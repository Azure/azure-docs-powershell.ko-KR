---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 3ef8248f90e24da8818a0fa1a8ff6b05970be397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524347"
---
# <span data-ttu-id="0ff71-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="0ff71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff71-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff71-103">네트워크 보안 그룹의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ff71-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ff71-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff71-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ff71-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff71-106">**AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="0ff71-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ff71-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff71-108">예제 1: 네트워크 보안 그룹의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="0ff71-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="0ff71-109">이 명령은 Nsg1 이라는 Azure 네트워크 보안 그룹을 가져오고 포트 3389의 인터넷 트래픽을 AzureRmNetworkSecurityRuleConfig 추가 기능을 사용 하 여 검색 된 네트워크 보안 그룹 개체로 허용 하는 Rdp-Rule 라는 네트워크 보안 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="0ff71-110">이 명령은 **Set-AzureRmNetworkSecurityGroup** 를 사용 하 여 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="0ff71-111">변수</span><span class="sxs-lookup"><span data-stu-id="0ff71-111">PARAMETERS</span></span>

### <span data-ttu-id="0ff71-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ff71-112">-AsJob</span></span>
<span data-ttu-id="0ff71-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0ff71-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff71-114">-DefaultProfile</span></span>
<span data-ttu-id="0ff71-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff71-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0ff71-117">Cmdlet이 네트워크 보안 그룹을 설정 하는 목표 상태를 나타내는 네트워크 보안 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff71-118">-확인</span><span class="sxs-lookup"><span data-stu-id="0ff71-118">-Confirm</span></span>
<span data-ttu-id="0ff71-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff71-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff71-120">-WhatIf</span></span>
<span data-ttu-id="0ff71-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ff71-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff71-123">CommonParameters</span></span>
<span data-ttu-id="0ff71-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ff71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff71-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff71-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff71-126">입력</span><span class="sxs-lookup"><span data-stu-id="0ff71-126">INPUTS</span></span>

### <span data-ttu-id="0ff71-127">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0ff71-128">매개 변수: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ff71-128">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="0ff71-129">출력</span><span class="sxs-lookup"><span data-stu-id="0ff71-129">OUTPUTS</span></span>

### <span data-ttu-id="0ff71-130">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-130">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0ff71-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0ff71-131">NOTES</span></span>

## <span data-ttu-id="0ff71-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ff71-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ff71-133">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-133">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0ff71-134">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-134">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0ff71-135">제거-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ff71-135">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


