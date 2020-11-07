---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 74da4bba721f415b48ee8ff626a1bfcf1d313b64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700531"
---
# <span data-ttu-id="c2ba5-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="c2ba5-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="c2ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ba5-103">구독의 네트워크 용도를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="c2ba5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2ba5-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2ba5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ba5-106">Get-AzNetworkUsage cmdlet은 네트워크 리소스에 대 한 제한 및 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="c2ba5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c2ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ba5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2ba5-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="c2ba5-109">Westcentralus 지역에서 리소스 사용 현황 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="c2ba5-110">변수</span><span class="sxs-lookup"><span data-stu-id="c2ba5-110">PARAMETERS</span></span>

### <span data-ttu-id="c2ba5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ba5-111">-DefaultProfile</span></span>
<span data-ttu-id="c2ba5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2ba5-113">-위치</span><span class="sxs-lookup"><span data-stu-id="c2ba5-113">-Location</span></span>
<span data-ttu-id="c2ba5-114">리소스 사용 현황을 쿼리 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ba5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ba5-115">CommonParameters</span></span>
<span data-ttu-id="c2ba5-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ba5-117">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2ba5-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ba5-118">입력</span><span class="sxs-lookup"><span data-stu-id="c2ba5-118">INPUTS</span></span>

### <span data-ttu-id="c2ba5-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2ba5-119">System.String</span></span>

## <span data-ttu-id="c2ba5-120">출력</span><span class="sxs-lookup"><span data-stu-id="c2ba5-120">OUTPUTS</span></span>

### <span data-ttu-id="c2ba5-121">Microsoft. Azure. PSUsage</span><span class="sxs-lookup"><span data-stu-id="c2ba5-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="c2ba5-122">상속자</span><span class="sxs-lookup"><span data-stu-id="c2ba5-122">NOTES</span></span>

## <span data-ttu-id="c2ba5-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2ba5-123">RELATED LINKS</span></span>