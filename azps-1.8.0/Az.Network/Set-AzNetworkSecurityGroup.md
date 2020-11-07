---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 78380af20ce5905b5c004424c1e17ac977de40ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699987"
---
# <span data-ttu-id="a2749-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a2749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2749-102">SYNOPSIS</span></span>
<span data-ttu-id="a2749-103">네트워크 보안 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-103">Updates a network security group.</span></span>

## <span data-ttu-id="a2749-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2749-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2749-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2749-105">DESCRIPTION</span></span>
<span data-ttu-id="a2749-106">**Set-AzNetworkSecurityGroup** cmdlet은 네트워크 보안 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="a2749-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2749-107">EXAMPLES</span></span>

### <span data-ttu-id="a2749-108">예제 1: 기존 네트워크 보안 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="a2749-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="a2749-109">이 명령은 Nsg1 이라는 Azure 네트워크 보안 그룹을 가져오고 포트 3389의 인터넷 트래픽을 AzNetworkSecurityRuleConfig 추가 기능을 사용 하 여 검색 된 네트워크 보안 그룹 개체로 허용 하는 Rdp-Rule 라는 네트워크 보안 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="a2749-110">이 명령은 **Set-AzNetworkSecurityGroup** 를 사용 하 여 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="a2749-111">변수</span><span class="sxs-lookup"><span data-stu-id="a2749-111">PARAMETERS</span></span>

### <span data-ttu-id="a2749-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2749-112">-AsJob</span></span>
<span data-ttu-id="a2749-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a2749-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2749-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2749-114">-DefaultProfile</span></span>
<span data-ttu-id="a2749-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2749-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a2749-117">네트워크 보안 그룹을 설정 해야 하는 상태를 나타내는 네트워크 보안 그룹 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="a2749-118">-확인</span><span class="sxs-lookup"><span data-stu-id="a2749-118">-Confirm</span></span>
<span data-ttu-id="a2749-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2749-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2749-120">-WhatIf</span></span>
<span data-ttu-id="a2749-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2749-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2749-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2749-123">CommonParameters</span></span>
<span data-ttu-id="a2749-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2749-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2749-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2749-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2749-126">입력</span><span class="sxs-lookup"><span data-stu-id="a2749-126">INPUTS</span></span>

### <span data-ttu-id="a2749-127">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a2749-128">출력</span><span class="sxs-lookup"><span data-stu-id="a2749-128">OUTPUTS</span></span>

### <span data-ttu-id="a2749-129">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a2749-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a2749-130">NOTES</span></span>

## <span data-ttu-id="a2749-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2749-131">RELATED LINKS</span></span>

[<span data-ttu-id="a2749-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a2749-133">새로운 AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a2749-134">제거-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2749-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


