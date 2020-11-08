---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226579"
---
# <span data-ttu-id="8d902-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d902-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8d902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d902-102">SYNOPSIS</span></span>
<span data-ttu-id="8d902-103">네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8d902-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d902-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d902-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d902-105">DESCRIPTION</span></span>
<span data-ttu-id="8d902-106">**AzNetworkSecurityRuleConfig** Cmdlet은 Azure 네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="8d902-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d902-107">EXAMPLES</span></span>

### <span data-ttu-id="8d902-108">1: 네트워크 보안 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d902-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="8d902-109">이 명령은 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹에서 "AllowInternetOutBound" 이라는 기본 규칙을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="8d902-110">2: 이름만 사용 하 여 네트워크 보안 규칙 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="8d902-111">이 명령은 리소스 그룹 "rg1"의 Azure 네트워크 보안 그룹 "nsg1"에서 ".rdp 규칙" 이라는 사용자 정의 규칙을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="8d902-112">변수</span><span class="sxs-lookup"><span data-stu-id="8d902-112">PARAMETERS</span></span>

### <span data-ttu-id="8d902-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d902-113">-DefaultProfile</span></span>
<span data-ttu-id="8d902-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d902-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="8d902-115">-DefaultRules</span></span>
<span data-ttu-id="8d902-116">이 cmdlet이 사용자가 만든 규칙 구성 또는 기본 규칙 구성을 가져올 것인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="8d902-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8d902-117">-Name</span></span>
<span data-ttu-id="8d902-118">가져올 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8d902-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d902-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8d902-120">가져올 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8d902-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d902-121">CommonParameters</span></span>
<span data-ttu-id="8d902-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d902-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d902-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d902-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d902-124">입력</span><span class="sxs-lookup"><span data-stu-id="8d902-124">INPUTS</span></span>

### <span data-ttu-id="8d902-125">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d902-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8d902-126">출력</span><span class="sxs-lookup"><span data-stu-id="8d902-126">OUTPUTS</span></span>

### <span data-ttu-id="8d902-127">Microsoft. 네트워크 모델. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="8d902-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="8d902-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8d902-128">NOTES</span></span>

## <span data-ttu-id="8d902-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d902-129">RELATED LINKS</span></span>

[<span data-ttu-id="8d902-130">추가-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d902-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8d902-131">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d902-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8d902-132">제거-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d902-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8d902-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d902-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


