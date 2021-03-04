---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: efe45da6cd5426fda3b301efd4daf2ef532e4c02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953739"
---
# <span data-ttu-id="0b326-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="0b326-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="0b326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b326-102">SYNOPSIS</span></span>
<span data-ttu-id="0b326-103">위치에 사용할 수 있는 SKU 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="0b326-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b326-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b326-105">설명</span><span class="sxs-lookup"><span data-stu-id="0b326-105">DESCRIPTION</span></span>
<span data-ttu-id="0b326-106">위치에 사용할 수 있는 SKU 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="0b326-107">예제</span><span class="sxs-lookup"><span data-stu-id="0b326-107">EXAMPLES</span></span>

### <span data-ttu-id="0b326-108">예제 1: 위치 이름에 따라 위치 기능 사용</span><span class="sxs-lookup"><span data-stu-id="0b326-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location eastus

SKU              Tier            Memory vCore
---              ----            ------ -----
Standard_B1ms    Burstable         2048     1
Standard_B2s     Burstable         2048     2
Standard_D2s_v3  GeneralPurpose    4096     2
Standard_D4s_v3  GeneralPurpose    4096     4
Standard_D8s_v3  GeneralPurpose    4096     8
Standard_D16s_v3 GeneralPurpose    4096    16
Standard_D32s_v3 GeneralPurpose    4096    32
Standard_D48s_v3 GeneralPurpose    4096    48
Standard_D64s_v3 GeneralPurpose    4096    64
Standard_E2s_v3  MemoryOptimized   8192     2
Standard_E4s_v3  MemoryOptimized   8192     4
Standard_E8s_v3  MemoryOptimized   8192     8
Standard_E16s_v3 MemoryOptimized   8192    16
Standard_E32s_v3 MemoryOptimized   8192    32
Standard_E48s_v3 MemoryOptimized   8192    48
Standard_E64s_v3 MemoryOptimized   6912    64
```

<span data-ttu-id="0b326-109">이 cmdlet은 제공된 위치의 기본 sku 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="0b326-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b326-110">PARAMETERS</span></span>

### <span data-ttu-id="0b326-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b326-111">-DefaultProfile</span></span>
<span data-ttu-id="0b326-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b326-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0b326-113">-Location</span></span>
<span data-ttu-id="0b326-114">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-114">The name of the location.</span></span>

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

### <span data-ttu-id="0b326-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b326-115">-SubscriptionId</span></span>
<span data-ttu-id="0b326-116">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b326-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b326-117">CommonParameters</span></span>
<span data-ttu-id="0b326-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b326-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b326-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b326-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b326-120">입력</span><span class="sxs-lookup"><span data-stu-id="0b326-120">INPUTS</span></span>

## <span data-ttu-id="0b326-121">출력</span><span class="sxs-lookup"><span data-stu-id="0b326-121">OUTPUTS</span></span>

### <span data-ttu-id="0b326-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="0b326-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="0b326-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b326-123">NOTES</span></span>

<span data-ttu-id="0b326-124">별칭</span><span class="sxs-lookup"><span data-stu-id="0b326-124">ALIASES</span></span>

## <span data-ttu-id="0b326-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b326-125">RELATED LINKS</span></span>

