---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 8a2851f34cfbeb9fec72830334c52a9b4a83d064
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875321"
---
# <span data-ttu-id="e7548-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7548-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e7548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7548-102">SYNOPSIS</span></span>
<span data-ttu-id="e7548-103">네트워크 보안 그룹에서 네트워크 보안 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="e7548-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7548-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7548-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7548-105">DESCRIPTION</span></span>
<span data-ttu-id="e7548-106">**AzNetworkSecurityRuleConfig** Cmdlet은 Azure 네트워크 보안 그룹에서 네트워크 보안 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="e7548-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7548-107">EXAMPLES</span></span>

### <span data-ttu-id="e7548-108">예제 1: 네트워크 보안 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="e7548-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="e7548-109">첫 번째 명령은 rdp 규칙 이라는 네트워크 보안 규칙 구성을 만든 다음이를 $rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="e7548-110">두 번째 명령은 $rule 1의 규칙을 사용 하 여 네트워크 보안 그룹을 만든 다음 네트워크 보안 그룹을 $nsg 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="e7548-111">세 번째 명령은 $nsg의 네트워크 보안 그룹에서 rdp 규칙 이라는 네트워크 보안 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="e7548-112">변수</span><span class="sxs-lookup"><span data-stu-id="e7548-112">PARAMETERS</span></span>

### <span data-ttu-id="e7548-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7548-113">-DefaultProfile</span></span>
<span data-ttu-id="e7548-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7548-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e7548-115">-Name</span></span>
<span data-ttu-id="e7548-116">이 cmdlet이 제거 하는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7548-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7548-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e7548-118">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="e7548-119">이 개체에는 제거할 네트워크 보안 규칙 구성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7548-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7548-120">CommonParameters</span></span>
<span data-ttu-id="e7548-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7548-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7548-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7548-123">입력</span><span class="sxs-lookup"><span data-stu-id="e7548-123">INPUTS</span></span>

### <span data-ttu-id="e7548-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7548-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="e7548-125">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7548-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="e7548-126">출력</span><span class="sxs-lookup"><span data-stu-id="e7548-126">OUTPUTS</span></span>

### <span data-ttu-id="e7548-127">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7548-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e7548-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e7548-128">NOTES</span></span>

## <span data-ttu-id="e7548-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7548-129">RELATED LINKS</span></span>

[<span data-ttu-id="e7548-130">추가-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7548-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7548-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7548-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7548-132">새로운 AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7548-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e7548-133">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7548-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7548-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7548-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


