---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711336"
---
# <span data-ttu-id="1d926-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="1d926-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="1d926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d926-102">SYNOPSIS</span></span>
<span data-ttu-id="1d926-103">사용할 수 있는 Azure 방화벽 Fqdn 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d926-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d926-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d926-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d926-105">DESCRIPTION</span></span>
<span data-ttu-id="1d926-106">**AzureRmFirewallFqdnTag** Cmdlet은 Azure 방화벽 응용 프로그램 규칙에 사용할 수 있는 FQDN 태그 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="1d926-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d926-107">EXAMPLES</span></span>

### <span data-ttu-id="1d926-108">1: 사용 가능한 모든 FQDN 태그 검색</span><span class="sxs-lookup"><span data-stu-id="1d926-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="1d926-109">이 예제에서는 사용 가능한 모든 FQDN 태그를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="1d926-110">2: 응용 프로그램 규칙에서 사용할 수 있는 첫 번째 FQDN 태그 사용</span><span class="sxs-lookup"><span data-stu-id="1d926-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="1d926-111">이 예제에서는 사용 가능한 첫 번째 FQDN 태그를 사용 하 여 방화벽 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="1d926-112">변수</span><span class="sxs-lookup"><span data-stu-id="1d926-112">PARAMETERS</span></span>

### <span data-ttu-id="1d926-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d926-113">-DefaultProfile</span></span>
<span data-ttu-id="1d926-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d926-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d926-115">CommonParameters</span></span>
<span data-ttu-id="1d926-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d926-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d926-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d926-118">입력</span><span class="sxs-lookup"><span data-stu-id="1d926-118">INPUTS</span></span>

### <span data-ttu-id="1d926-119">않아야</span><span class="sxs-lookup"><span data-stu-id="1d926-119">None</span></span>
<span data-ttu-id="1d926-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d926-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d926-121">출력</span><span class="sxs-lookup"><span data-stu-id="1d926-121">OUTPUTS</span></span>

### <span data-ttu-id="1d926-122">PSAzureFirewallFqdnTag에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1d926-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="1d926-123">상속자</span><span class="sxs-lookup"><span data-stu-id="1d926-123">NOTES</span></span>

## <span data-ttu-id="1d926-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d926-124">RELATED LINKS</span></span>

[<span data-ttu-id="1d926-125">새로운 AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1d926-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="1d926-126">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1d926-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
