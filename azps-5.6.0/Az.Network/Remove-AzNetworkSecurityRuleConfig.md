---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a60fa0e305d05ae5d944a69705c3cb3f392b28f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993617"
---
# <span data-ttu-id="0fbaa-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0fbaa-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0fbaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbaa-103">네트워크 보안 그룹에서 네트워크 보안 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="0fbaa-104">구문</span><span class="sxs-lookup"><span data-stu-id="0fbaa-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbaa-105">설명</span><span class="sxs-lookup"><span data-stu-id="0fbaa-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbaa-106">**Remove-AzNetworkSecurityRuleConfig** cmdlet은 Azure 네트워크 보안 그룹에서 네트워크 보안 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="0fbaa-107">예제</span><span class="sxs-lookup"><span data-stu-id="0fbaa-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbaa-108">예제 1: 네트워크 보안 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="0fbaa-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="0fbaa-109">첫 번째 명령은 rdp-rule이라는 네트워크 보안 규칙 구성을 만든 다음, $rule 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="0fbaa-110">두 번째 명령은 $rule 1의 규칙을 사용하여 네트워크 보안 그룹을 만든 다음, 네트워크 보안 그룹을 $nsg 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="0fbaa-111">세 번째 명령은 네트워크 보안 그룹에서 rdp-rule이라는 네트워크 보안 규칙 구성을 $nsg.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="0fbaa-112">첫 번째 명령은 변경을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-112">The forth command saves the change.</span></span>

## <span data-ttu-id="0fbaa-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0fbaa-113">PARAMETERS</span></span>

### <span data-ttu-id="0fbaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbaa-114">-DefaultProfile</span></span>
<span data-ttu-id="0fbaa-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbaa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0fbaa-116">-Name</span></span>
<span data-ttu-id="0fbaa-117">이 cmdlet이 제거하는 네트워크 보안 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0fbaa-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0fbaa-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0fbaa-119">**NetworkSecurityGroup 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="0fbaa-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="0fbaa-120">이 개체에는 제거할 네트워크 보안 규칙 구성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="0fbaa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbaa-121">CommonParameters</span></span>
<span data-ttu-id="0fbaa-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbaa-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0fbaa-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbaa-124">입력</span><span class="sxs-lookup"><span data-stu-id="0fbaa-124">INPUTS</span></span>

### <span data-ttu-id="0fbaa-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0fbaa-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0fbaa-126">출력</span><span class="sxs-lookup"><span data-stu-id="0fbaa-126">OUTPUTS</span></span>

### <span data-ttu-id="0fbaa-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0fbaa-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0fbaa-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0fbaa-128">NOTES</span></span>

## <span data-ttu-id="0fbaa-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fbaa-129">RELATED LINKS</span></span>

[<span data-ttu-id="0fbaa-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0fbaa-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0fbaa-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0fbaa-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0fbaa-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0fbaa-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="0fbaa-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0fbaa-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0fbaa-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0fbaa-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


