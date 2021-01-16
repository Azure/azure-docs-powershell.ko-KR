---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346557"
---
# <span data-ttu-id="47478-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="47478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47478-102">SYNOPSIS</span></span>
<span data-ttu-id="47478-103">네트워크 보안 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47478-103">Updates a network security group.</span></span>

## <span data-ttu-id="47478-104">구문</span><span class="sxs-lookup"><span data-stu-id="47478-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47478-105">설명</span><span class="sxs-lookup"><span data-stu-id="47478-105">DESCRIPTION</span></span>
<span data-ttu-id="47478-106">**Set-AzNetworkSecurityGroup** cmdlet은 네트워크 보안 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47478-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="47478-107">예제</span><span class="sxs-lookup"><span data-stu-id="47478-107">EXAMPLES</span></span>

### <span data-ttu-id="47478-108">예제 1: 기존 네트워크 보안 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="47478-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="47478-109">이 명령은 Nsg1이라는 Azure 네트워크 보안 그룹을 가져온 다음 Rdp-Rule 포트 3389의 인터넷 트래픽을 Add-AzNetworkSecurityRuleConfig를 사용하여 검색된 네트워크 보안 그룹 개체에 허용하는 네트워크 보안 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47478-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="47478-110">이 명령은 **Set-AzNetworkSecurityGroup을** 사용하여 수정된 Azure 네트워크 보안 그룹을 유지 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="47478-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="47478-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47478-111">PARAMETERS</span></span>

### <span data-ttu-id="47478-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47478-112">-AsJob</span></span>
<span data-ttu-id="47478-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="47478-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47478-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47478-114">-DefaultProfile</span></span>
<span data-ttu-id="47478-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47478-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47478-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="47478-117">네트워크 보안 그룹을 설정해야 하는 상태를 나타내는 네트워크 보안 그룹 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47478-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="47478-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47478-118">-Confirm</span></span>
<span data-ttu-id="47478-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47478-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47478-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47478-120">-WhatIf</span></span>
<span data-ttu-id="47478-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="47478-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47478-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47478-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47478-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47478-123">CommonParameters</span></span>
<span data-ttu-id="47478-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47478-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47478-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="47478-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47478-126">입력</span><span class="sxs-lookup"><span data-stu-id="47478-126">INPUTS</span></span>

### <span data-ttu-id="47478-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="47478-128">출력</span><span class="sxs-lookup"><span data-stu-id="47478-128">OUTPUTS</span></span>

### <span data-ttu-id="47478-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="47478-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47478-130">NOTES</span></span>

## <span data-ttu-id="47478-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47478-131">RELATED LINKS</span></span>

[<span data-ttu-id="47478-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="47478-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="47478-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="47478-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


