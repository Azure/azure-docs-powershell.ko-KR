---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: a4d8386cdcdee8b67bea746e40a9035acf3bcce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711810"
---
# <span data-ttu-id="c4128-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4128-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c4128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4128-102">SYNOPSIS</span></span>
<span data-ttu-id="c4128-103">네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4128-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4128-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4128-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4128-105">DESCRIPTION</span></span>
<span data-ttu-id="c4128-106">**AzureRmNetworkSecurityRuleConfig** Cmdlet은 Azure 네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="c4128-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4128-107">EXAMPLES</span></span>

### <span data-ttu-id="c4128-108">1: 네트워크 보안 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="c4128-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="c4128-109">이 명령은 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹에서 "AllowInternetOutBound" 이라는 기본 규칙을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="c4128-110">2: 이름만 사용 하 여 네트워크 보안 규칙 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="c4128-111">이 명령은 리소스 그룹 "rg1"의 Azure 네트워크 보안 그룹 "nsg1"에서 ".rdp 규칙" 이라는 사용자 정의 규칙을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="c4128-112">변수</span><span class="sxs-lookup"><span data-stu-id="c4128-112">PARAMETERS</span></span>

### <span data-ttu-id="c4128-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4128-113">-DefaultProfile</span></span>
<span data-ttu-id="c4128-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4128-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="c4128-115">-DefaultRules</span></span>
<span data-ttu-id="c4128-116">이 cmdlet이 사용자가 만든 규칙 구성 또는 기본 규칙 구성을 가져올 것인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="c4128-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c4128-117">-Name</span></span>
<span data-ttu-id="c4128-118">가져올 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="c4128-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4128-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c4128-120">가져올 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="c4128-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4128-121">CommonParameters</span></span>
<span data-ttu-id="c4128-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4128-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4128-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4128-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4128-124">입력</span><span class="sxs-lookup"><span data-stu-id="c4128-124">INPUTS</span></span>

### <span data-ttu-id="c4128-125">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4128-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="c4128-126">매개 변수: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4128-126">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="c4128-127">출력</span><span class="sxs-lookup"><span data-stu-id="c4128-127">OUTPUTS</span></span>

### <span data-ttu-id="c4128-128">Microsoft. 네트워크 모델. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="c4128-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="c4128-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c4128-129">NOTES</span></span>

## <span data-ttu-id="c4128-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4128-130">RELATED LINKS</span></span>

[<span data-ttu-id="c4128-131">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4128-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4128-132">새로운 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4128-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4128-133">제거-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4128-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4128-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4128-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


