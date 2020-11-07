---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 9aed668c977fc1156e2a52723273b1d6d37fba71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881797"
---
# <span data-ttu-id="8ef3b-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ef3b-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8ef3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef3b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef3b-103">네트워크 보안 그룹에서 네트워크 보안 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ef3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ef3b-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ef3b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ef3b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef3b-106">**AzureRmNetworkSecurityRuleConfig** Cmdlet은 Azure 네트워크 보안 그룹에서 네트워크 보안 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="8ef3b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ef3b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ef3b-108">예제 1: 네트워크 보안 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="8ef3b-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="8ef3b-109">첫 번째 명령은 rdp 규칙 이라는 네트워크 보안 규칙 구성을 만든 다음이를 $rule 1 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="8ef3b-110">두 번째 명령은 $rule 1의 규칙을 사용 하 여 네트워크 보안 그룹을 만든 다음 네트워크 보안 그룹을 $nsg 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="8ef3b-111">세 번째 명령은 $nsg의 네트워크 보안 그룹에서 rdp 규칙 이라는 네트워크 보안 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="8ef3b-112">변수</span><span class="sxs-lookup"><span data-stu-id="8ef3b-112">PARAMETERS</span></span>

### <span data-ttu-id="8ef3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef3b-113">-DefaultProfile</span></span>
<span data-ttu-id="8ef3b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ef3b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8ef3b-115">-Name</span></span>
<span data-ttu-id="8ef3b-116">이 cmdlet이 제거 하는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ef3b-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8ef3b-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8ef3b-118">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="8ef3b-119">이 개체에는 제거할 네트워크 보안 규칙 구성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="8ef3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef3b-120">CommonParameters</span></span>
<span data-ttu-id="8ef3b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef3b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef3b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef3b-123">입력</span><span class="sxs-lookup"><span data-stu-id="8ef3b-123">INPUTS</span></span>

### <span data-ttu-id="8ef3b-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8ef3b-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="8ef3b-125">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="8ef3b-126">출력</span><span class="sxs-lookup"><span data-stu-id="8ef3b-126">OUTPUTS</span></span>

### <span data-ttu-id="8ef3b-127">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8ef3b-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8ef3b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8ef3b-128">NOTES</span></span>

## <span data-ttu-id="8ef3b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ef3b-129">RELATED LINKS</span></span>

[<span data-ttu-id="8ef3b-130">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ef3b-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8ef3b-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ef3b-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8ef3b-132">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8ef3b-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="8ef3b-133">새로운 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ef3b-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8ef3b-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ef3b-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


