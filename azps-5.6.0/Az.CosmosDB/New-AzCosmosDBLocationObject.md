---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 829bd1f01be1226346d67f9b662915675cd70f80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986869"
---
# <span data-ttu-id="a483e-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="a483e-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="a483e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a483e-102">SYNOPSIS</span></span>
<span data-ttu-id="a483e-103">새 CosmosDB 위치 개체(PSLocation)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="a483e-104">구문</span><span class="sxs-lookup"><span data-stu-id="a483e-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a483e-105">설명</span><span class="sxs-lookup"><span data-stu-id="a483e-105">DESCRIPTION</span></span>
<span data-ttu-id="a483e-106">새 CosmosDB 위치 개체(PSLocation)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="a483e-107">예제</span><span class="sxs-lookup"><span data-stu-id="a483e-107">EXAMPLES</span></span>

### <span data-ttu-id="a483e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a483e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="a483e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a483e-109">PARAMETERS</span></span>

### <span data-ttu-id="a483e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a483e-110">-DefaultProfile</span></span>
<span data-ttu-id="a483e-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a483e-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="a483e-112">-FailoverPriority</span></span>
<span data-ttu-id="a483e-113">위치의 장애 조치 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a483e-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a483e-114">-IsZoneRedundant</span></span>
<span data-ttu-id="a483e-115">이 지역이 AvailabilityZone인지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a483e-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="a483e-116">-LocationName</span></span>
<span data-ttu-id="a483e-117">문자열의 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-117">Name of the Location in string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a483e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a483e-118">CommonParameters</span></span>
<span data-ttu-id="a483e-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a483e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a483e-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a483e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a483e-121">입력</span><span class="sxs-lookup"><span data-stu-id="a483e-121">INPUTS</span></span>

### <span data-ttu-id="a483e-122">없음</span><span class="sxs-lookup"><span data-stu-id="a483e-122">None</span></span>

## <span data-ttu-id="a483e-123">출력</span><span class="sxs-lookup"><span data-stu-id="a483e-123">OUTPUTS</span></span>

### <span data-ttu-id="a483e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="a483e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="a483e-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a483e-125">NOTES</span></span>

## <span data-ttu-id="a483e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a483e-126">RELATED LINKS</span></span>
