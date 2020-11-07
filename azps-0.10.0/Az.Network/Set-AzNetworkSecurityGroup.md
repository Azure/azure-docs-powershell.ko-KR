---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876569"
---
# <span data-ttu-id="db396-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="db396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db396-102">SYNOPSIS</span></span>
<span data-ttu-id="db396-103">네트워크 보안 그룹의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db396-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="db396-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db396-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db396-105">설명은</span><span class="sxs-lookup"><span data-stu-id="db396-105">DESCRIPTION</span></span>
<span data-ttu-id="db396-106">**AzNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db396-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="db396-107">예제의</span><span class="sxs-lookup"><span data-stu-id="db396-107">EXAMPLES</span></span>

### <span data-ttu-id="db396-108">예제 1: 네트워크 보안 그룹의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="db396-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="db396-109">이 명령은 Nsg1 이라는 Azure 네트워크 보안 그룹을 가져오고 포트 3389의 인터넷 트래픽을 AzNetworkSecurityRuleConfig 추가 기능을 사용 하 여 검색 된 네트워크 보안 그룹 개체로 허용 하는 Rdp-Rule 라는 네트워크 보안 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="db396-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="db396-110">이 명령은 **Set-AzNetworkSecurityGroup** 를 사용 하 여 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="db396-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="db396-111">변수</span><span class="sxs-lookup"><span data-stu-id="db396-111">PARAMETERS</span></span>

### <span data-ttu-id="db396-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db396-112">-AsJob</span></span>
<span data-ttu-id="db396-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="db396-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db396-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db396-114">-DefaultProfile</span></span>
<span data-ttu-id="db396-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db396-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db396-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="db396-117">Cmdlet이 네트워크 보안 그룹을 설정 하는 목표 상태를 나타내는 네트워크 보안 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db396-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="db396-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db396-118">CommonParameters</span></span>
<span data-ttu-id="db396-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db396-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db396-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db396-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db396-121">입력</span><span class="sxs-lookup"><span data-stu-id="db396-121">INPUTS</span></span>

### <span data-ttu-id="db396-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="db396-123">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db396-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="db396-124">출력</span><span class="sxs-lookup"><span data-stu-id="db396-124">OUTPUTS</span></span>

### <span data-ttu-id="db396-125">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="db396-126">상속자</span><span class="sxs-lookup"><span data-stu-id="db396-126">NOTES</span></span>

## <span data-ttu-id="db396-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db396-127">RELATED LINKS</span></span>

[<span data-ttu-id="db396-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="db396-129">새로운 AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="db396-130">제거-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db396-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


