---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379947"
---
# <span data-ttu-id="975d0-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="975d0-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="975d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="975d0-102">SYNOPSIS</span></span>
<span data-ttu-id="975d0-103">구독에 대한 네트워크 사용량을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="975d0-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="975d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="975d0-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="975d0-105">설명</span><span class="sxs-lookup"><span data-stu-id="975d0-105">DESCRIPTION</span></span>
<span data-ttu-id="975d0-106">이 Get-AzNetworkUsage cmdlet은 네트워크 리소스에 대한 제한 및 현재 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="975d0-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="975d0-107">예제</span><span class="sxs-lookup"><span data-stu-id="975d0-107">EXAMPLES</span></span>

### <span data-ttu-id="975d0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="975d0-108">Example 1</span></span>
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

<span data-ttu-id="975d0-109">westcentralus 지역의 리소스 사용량 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="975d0-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="975d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="975d0-110">PARAMETERS</span></span>

### <span data-ttu-id="975d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975d0-111">-DefaultProfile</span></span>
<span data-ttu-id="975d0-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="975d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="975d0-113">-Location</span><span class="sxs-lookup"><span data-stu-id="975d0-113">-Location</span></span>
<span data-ttu-id="975d0-114">리소스 사용량이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975d0-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="975d0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975d0-115">CommonParameters</span></span>
<span data-ttu-id="975d0-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="975d0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975d0-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="975d0-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975d0-118">입력</span><span class="sxs-lookup"><span data-stu-id="975d0-118">INPUTS</span></span>

### <span data-ttu-id="975d0-119">System.String</span><span class="sxs-lookup"><span data-stu-id="975d0-119">System.String</span></span>

## <span data-ttu-id="975d0-120">출력</span><span class="sxs-lookup"><span data-stu-id="975d0-120">OUTPUTS</span></span>

### <span data-ttu-id="975d0-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="975d0-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="975d0-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="975d0-122">NOTES</span></span>

## <span data-ttu-id="975d0-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="975d0-123">RELATED LINKS</span></span>
