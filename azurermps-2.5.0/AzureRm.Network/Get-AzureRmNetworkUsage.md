---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkusage
schema: 2.0.0
ms.openlocfilehash: 24ffdb99efddf22a5e632ac576a4aa8e7db42af6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881018"
---
# <span data-ttu-id="b37b8-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="b37b8-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="b37b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b37b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b37b8-103">구독의 네트워크 용도를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b37b8-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b37b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b37b8-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b37b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b37b8-105">DESCRIPTION</span></span>
<span data-ttu-id="b37b8-106">Get-AzureRmNetworkUsage cmdlet은 네트워크 리소스에 대 한 제한 및 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b37b8-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="b37b8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b37b8-107">EXAMPLES</span></span>

### <span data-ttu-id="b37b8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b37b8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

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

<span data-ttu-id="b37b8-109">Westcentralus 지역에서 리소스 사용 현황 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b37b8-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="b37b8-110">변수</span><span class="sxs-lookup"><span data-stu-id="b37b8-110">PARAMETERS</span></span>

### <span data-ttu-id="b37b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37b8-111">-DefaultProfile</span></span>
<span data-ttu-id="b37b8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b37b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b37b8-113">-위치</span><span class="sxs-lookup"><span data-stu-id="b37b8-113">-Location</span></span>
<span data-ttu-id="b37b8-114">리소스 사용 현황을 쿼리 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b37b8-114">The location where resource usage is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37b8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37b8-115">CommonParameters</span></span>
<span data-ttu-id="b37b8-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b37b8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37b8-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b37b8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37b8-118">입력</span><span class="sxs-lookup"><span data-stu-id="b37b8-118">INPUTS</span></span>

### <span data-ttu-id="b37b8-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b37b8-119">System.String</span></span>

## <span data-ttu-id="b37b8-120">출력</span><span class="sxs-lookup"><span data-stu-id="b37b8-120">OUTPUTS</span></span>

### <span data-ttu-id="b37b8-121">Microsoft. Azure. PSUsage</span><span class="sxs-lookup"><span data-stu-id="b37b8-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="b37b8-122">상속자</span><span class="sxs-lookup"><span data-stu-id="b37b8-122">NOTES</span></span>

## <span data-ttu-id="b37b8-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b37b8-123">RELATED LINKS</span></span>
