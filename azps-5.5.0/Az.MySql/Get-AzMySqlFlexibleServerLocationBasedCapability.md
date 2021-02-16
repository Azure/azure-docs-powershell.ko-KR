---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 20c142df2a3df0ea6448c2bcb58ad47169d9e483
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180092"
---
# <span data-ttu-id="52813-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="52813-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="52813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52813-102">SYNOPSIS</span></span>
<span data-ttu-id="52813-103">위치에 사용 가능한 SKU 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52813-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="52813-104">구문</span><span class="sxs-lookup"><span data-stu-id="52813-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="52813-105">설명</span><span class="sxs-lookup"><span data-stu-id="52813-105">DESCRIPTION</span></span>
<span data-ttu-id="52813-106">위치에 사용 가능한 SKU 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52813-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="52813-107">예제</span><span class="sxs-lookup"><span data-stu-id="52813-107">EXAMPLES</span></span>

### <span data-ttu-id="52813-108">예제 1: 위치 이름에 따라 위치 기능 얻기</span><span class="sxs-lookup"><span data-stu-id="52813-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerLocationBasedCapability -Location westus2
"Please refer to https://aka.ms/mysql-pricing for pricing details"

SKU               Tier            Memory vCore
---               ----            ------ -----
Standard_B1s      Burstable         1024     1
Standard_B1ms     Burstable         2048     1
Standard_B2s      Burstable         2048     2
Standard_D2ds_v4  GeneralPurpose    4096     2
Standard_D4ds_v4  GeneralPurpose    4096     4
Standard_D8ds_v4  GeneralPurpose    4096     8
Standard_D16ds_v4 GeneralPurpose    4096    16
Standard_D32ds_v4 GeneralPurpose    4096    32
Standard_D48ds_v4 GeneralPurpose    4096    48
Standard_D64ds_v4 GeneralPurpose    4096    64
Standard_E2ds_v4  MemoryOptimized   8192     2
Standard_E4ds_v4  MemoryOptimized   8192     4
Standard_E8ds_v4  MemoryOptimized   8192     8
Standard_E16ds_v4 MemoryOptimized   8192    16
Standard_E32ds_v4 MemoryOptimized   8192    32
Standard_E48ds_v4 MemoryOptimized   8192    48
Standard_E64ds_v4 MemoryOptimized   8192    64

```

<span data-ttu-id="52813-109">이 cmdlet은 제공된 위치의 기본 SKU 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="52813-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="52813-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52813-110">PARAMETERS</span></span>

### <span data-ttu-id="52813-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52813-111">-DefaultProfile</span></span>
<span data-ttu-id="52813-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52813-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52813-113">-Location</span><span class="sxs-lookup"><span data-stu-id="52813-113">-Location</span></span>
<span data-ttu-id="52813-114">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52813-114">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52813-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52813-115">-SubscriptionId</span></span>
<span data-ttu-id="52813-116">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="52813-116">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52813-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52813-117">CommonParameters</span></span>
<span data-ttu-id="52813-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52813-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52813-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52813-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52813-120">입력</span><span class="sxs-lookup"><span data-stu-id="52813-120">INPUTS</span></span>

## <span data-ttu-id="52813-121">출력</span><span class="sxs-lookup"><span data-stu-id="52813-121">OUTPUTS</span></span>

### <span data-ttu-id="52813-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="52813-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="52813-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52813-123">NOTES</span></span>

<span data-ttu-id="52813-124">별칭</span><span class="sxs-lookup"><span data-stu-id="52813-124">ALIASES</span></span>

## <span data-ttu-id="52813-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52813-125">RELATED LINKS</span></span>

