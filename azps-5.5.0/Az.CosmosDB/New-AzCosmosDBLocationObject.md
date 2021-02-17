---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204632"
---
# <span data-ttu-id="28352-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="28352-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="28352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28352-102">SYNOPSIS</span></span>
<span data-ttu-id="28352-103">새 CosmosDB 위치 개체(PSLocation)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28352-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="28352-104">구문</span><span class="sxs-lookup"><span data-stu-id="28352-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28352-105">설명</span><span class="sxs-lookup"><span data-stu-id="28352-105">DESCRIPTION</span></span>
<span data-ttu-id="28352-106">새 CosmosDB 위치 개체(PSLocation)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28352-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="28352-107">예제</span><span class="sxs-lookup"><span data-stu-id="28352-107">EXAMPLES</span></span>

### <span data-ttu-id="28352-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="28352-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="28352-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28352-109">PARAMETERS</span></span>

### <span data-ttu-id="28352-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28352-110">-DefaultProfile</span></span>
<span data-ttu-id="28352-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28352-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28352-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="28352-112">-FailoverPriority</span></span>
<span data-ttu-id="28352-113">위치의 장애 조치 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="28352-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="28352-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="28352-114">-IsZoneRedundant</span></span>
<span data-ttu-id="28352-115">이 지역이 AvailabilityZone인지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="28352-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="28352-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="28352-116">-LocationName</span></span>
<span data-ttu-id="28352-117">문자열의 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28352-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="28352-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28352-118">CommonParameters</span></span>
<span data-ttu-id="28352-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28352-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28352-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28352-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28352-121">입력</span><span class="sxs-lookup"><span data-stu-id="28352-121">INPUTS</span></span>

### <span data-ttu-id="28352-122">없음</span><span class="sxs-lookup"><span data-stu-id="28352-122">None</span></span>

## <span data-ttu-id="28352-123">출력</span><span class="sxs-lookup"><span data-stu-id="28352-123">OUTPUTS</span></span>

### <span data-ttu-id="28352-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="28352-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="28352-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28352-125">NOTES</span></span>

## <span data-ttu-id="28352-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28352-126">RELATED LINKS</span></span>
