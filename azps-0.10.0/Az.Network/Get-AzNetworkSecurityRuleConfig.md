---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 184e1291f134b52ee57a239327bb45da4a4481ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875561"
---
# <span data-ttu-id="8f758-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8f758-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8f758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f758-102">SYNOPSIS</span></span>
<span data-ttu-id="8f758-103">네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8f758-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f758-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f758-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f758-105">DESCRIPTION</span></span>
<span data-ttu-id="8f758-106">**AzNetworkSecurityRuleConfig** Cmdlet은 Azure 네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="8f758-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8f758-107">EXAMPLES</span></span>

### <span data-ttu-id="8f758-108">1: 네트워크 보안 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8f758-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="8f758-109">이 명령은 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹에서 "AllowInternetOutBound" 이라는 기본 규칙을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="8f758-110">2: 이름만 사용 하 여 네트워크 보안 규칙 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="8f758-111">이 명령은 리소스 그룹 "rg1"의 Azure 네트워크 보안 그룹 "nsg1"에서 ".rdp 규칙" 이라는 사용자 정의 규칙을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="8f758-112">변수</span><span class="sxs-lookup"><span data-stu-id="8f758-112">PARAMETERS</span></span>

### <span data-ttu-id="8f758-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f758-113">-DefaultProfile</span></span>
<span data-ttu-id="8f758-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f758-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="8f758-115">-DefaultRules</span></span>
<span data-ttu-id="8f758-116">이 cmdlet이 사용자가 만든 규칙 구성 또는 기본 규칙 구성을 가져올 것인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f758-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8f758-117">-Name</span></span>
<span data-ttu-id="8f758-118">가져올 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8f758-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f758-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8f758-120">가져올 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8f758-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f758-121">CommonParameters</span></span>
<span data-ttu-id="8f758-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f758-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f758-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f758-124">입력</span><span class="sxs-lookup"><span data-stu-id="8f758-124">INPUTS</span></span>

### <span data-ttu-id="8f758-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f758-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="8f758-126">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f758-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="8f758-127">출력</span><span class="sxs-lookup"><span data-stu-id="8f758-127">OUTPUTS</span></span>

### <span data-ttu-id="8f758-128">Microsoft. 네트워크 모델. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="8f758-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="8f758-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8f758-129">NOTES</span></span>

## <span data-ttu-id="8f758-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f758-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f758-131">추가-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8f758-131">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8f758-132">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8f758-132">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8f758-133">제거-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8f758-133">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8f758-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8f758-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


