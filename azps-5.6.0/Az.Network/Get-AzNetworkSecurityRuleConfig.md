---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: c45df01f86abcd7a2f475b62b517765f3045cb10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006320"
---
# <span data-ttu-id="0ad1b-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ad1b-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0ad1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad1b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad1b-103">네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="0ad1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ad1b-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad1b-105">설명</span><span class="sxs-lookup"><span data-stu-id="0ad1b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad1b-106">**Get-AzNetworkSecurityRuleConfig** cmdlet은 Azure 네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="0ad1b-107">예제</span><span class="sxs-lookup"><span data-stu-id="0ad1b-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad1b-108">1: 네트워크 보안 규칙 구성 검색</span><span class="sxs-lookup"><span data-stu-id="0ad1b-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="0ad1b-109">이 명령은 리소스 그룹 "rg1"에서 "nsg1"이라는 Azure 네트워크 보안 그룹에서 "AllowInternetOutBound"이라는 기본 규칙을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="0ad1b-110">2: 이름만 사용하여 네트워크 보안 규칙 구성 검색</span><span class="sxs-lookup"><span data-stu-id="0ad1b-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="0ad1b-111">이 명령은 리소스 그룹 "rg1"에서 "nsg1"이라는 Azure 네트워크 보안 그룹에서 "rdp-rule"이라는 사용자 정의 규칙을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="0ad1b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ad1b-112">PARAMETERS</span></span>

### <span data-ttu-id="0ad1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad1b-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad1b-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad1b-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="0ad1b-115">-DefaultRules</span></span>
<span data-ttu-id="0ad1b-116">이 cmdlet이 사용자 만든 규칙 구성을 얻거나 기본 규칙 구성을 얻을지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="0ad1b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0ad1b-117">-Name</span></span>
<span data-ttu-id="0ad1b-118">얻을 네트워크 보안 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="0ad1b-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ad1b-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0ad1b-120">얻을 네트워크 보안 규칙 구성을 포함하는 **NetworkSecurityGroup** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="0ad1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad1b-121">CommonParameters</span></span>
<span data-ttu-id="0ad1b-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad1b-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ad1b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad1b-124">입력</span><span class="sxs-lookup"><span data-stu-id="0ad1b-124">INPUTS</span></span>

### <span data-ttu-id="0ad1b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0ad1b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0ad1b-126">출력</span><span class="sxs-lookup"><span data-stu-id="0ad1b-126">OUTPUTS</span></span>

### <span data-ttu-id="0ad1b-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="0ad1b-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="0ad1b-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ad1b-128">NOTES</span></span>

## <span data-ttu-id="0ad1b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ad1b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ad1b-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ad1b-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0ad1b-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ad1b-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0ad1b-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ad1b-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0ad1b-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ad1b-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


