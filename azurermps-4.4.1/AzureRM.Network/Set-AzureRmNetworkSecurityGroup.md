---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529270"
---
# <span data-ttu-id="d5683-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="d5683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5683-102">SYNOPSIS</span></span>
<span data-ttu-id="d5683-103">네트워크 보안 그룹의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5683-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5683-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5683-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5683-105">DESCRIPTION</span></span>
<span data-ttu-id="d5683-106">**AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="d5683-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5683-107">EXAMPLES</span></span>

### <span data-ttu-id="d5683-108">예제 1: 네트워크 보안 그룹의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="d5683-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="d5683-109">이 명령은 Nsg1 이라는 Azure 네트워크 보안 그룹을 가져오고 포트 3389의 인터넷 트래픽을 AzureRmNetworkSecurityRuleConfig 추가 기능을 사용 하 여 검색 된 네트워크 보안 그룹 개체로 허용 하는 Rdp-Rule 라는 네트워크 보안 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="d5683-110">이 명령은 **Set-AzureRmNetworkSecurityGroup** 를 사용 하 여 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="d5683-111">변수</span><span class="sxs-lookup"><span data-stu-id="d5683-111">PARAMETERS</span></span>

### <span data-ttu-id="d5683-112">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-112">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d5683-113">Cmdlet이 네트워크 보안 그룹을 설정 하는 목표 상태를 나타내는 네트워크 보안 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-113">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="d5683-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5683-114">-DefaultProfile</span></span>
<span data-ttu-id="d5683-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5683-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5683-116">CommonParameters</span></span>
<span data-ttu-id="d5683-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5683-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5683-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5683-119">입력</span><span class="sxs-lookup"><span data-stu-id="d5683-119">INPUTS</span></span>

### <span data-ttu-id="d5683-120">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-120">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="d5683-121">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5683-121">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="d5683-122">출력</span><span class="sxs-lookup"><span data-stu-id="d5683-122">OUTPUTS</span></span>

### <span data-ttu-id="d5683-123">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-123">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d5683-124">상속자</span><span class="sxs-lookup"><span data-stu-id="d5683-124">NOTES</span></span>

## <span data-ttu-id="d5683-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5683-125">RELATED LINKS</span></span>

[<span data-ttu-id="d5683-126">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-126">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d5683-127">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-127">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d5683-128">제거-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5683-128">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


