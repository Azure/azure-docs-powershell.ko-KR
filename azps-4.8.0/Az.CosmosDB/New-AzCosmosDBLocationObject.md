---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048377"
---
# <span data-ttu-id="b5c72-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="b5c72-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="b5c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c72-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c72-103">새 CosmosDB Location 개체 (PSLocation)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="b5c72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5c72-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c72-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5c72-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c72-106">새 CosmosDB Location 개체 (PSLocation)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="b5c72-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5c72-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c72-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5c72-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="b5c72-109">변수</span><span class="sxs-lookup"><span data-stu-id="b5c72-109">PARAMETERS</span></span>

### <span data-ttu-id="b5c72-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c72-110">-DefaultProfile</span></span>
<span data-ttu-id="b5c72-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c72-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="b5c72-112">-FailoverPriority</span></span>
<span data-ttu-id="b5c72-113">위치에 대 한 장애 조치 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="b5c72-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b5c72-114">-IsZoneRedundant</span></span>
<span data-ttu-id="b5c72-115">이 지역이 AvailabilityZone 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="b5c72-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="b5c72-116">-LocationName</span></span>
<span data-ttu-id="b5c72-117">문자열 내의 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="b5c72-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c72-118">CommonParameters</span></span>
<span data-ttu-id="b5c72-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c72-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c72-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5c72-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c72-121">입력</span><span class="sxs-lookup"><span data-stu-id="b5c72-121">INPUTS</span></span>

### <span data-ttu-id="b5c72-122">않아야</span><span class="sxs-lookup"><span data-stu-id="b5c72-122">None</span></span>

## <span data-ttu-id="b5c72-123">출력</span><span class="sxs-lookup"><span data-stu-id="b5c72-123">OUTPUTS</span></span>

### <span data-ttu-id="b5c72-124">CosmosDB (.) PSLocation</span><span class="sxs-lookup"><span data-stu-id="b5c72-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="b5c72-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b5c72-125">NOTES</span></span>

## <span data-ttu-id="b5c72-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5c72-126">RELATED LINKS</span></span>
