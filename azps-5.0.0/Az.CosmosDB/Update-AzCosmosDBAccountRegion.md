---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306848"
---
# <span data-ttu-id="fde32-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="fde32-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="fde32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde32-102">SYNOPSIS</span></span>
<span data-ttu-id="fde32-103">CosmosDB 계정의 지역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="fde32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fde32-104">SYNTAX</span></span>

### <span data-ttu-id="fde32-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fde32-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fde32-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fde32-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde32-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fde32-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde32-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fde32-108">DESCRIPTION</span></span>
<span data-ttu-id="fde32-109">CosmosDB 계정의 지역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="fde32-110">위치는 PSLocation 형식의 개체 또는 장애 조치 우선 순위로 정렬 된 위치 이름 문자열로 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="fde32-111">LocationObject 매개 변수는 새 위치에 해당 하는 새 Locationobject에 의해 추가 되는 현재 위치 (장애 조치 prioritiies 포함)의 목록을 필요로 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="fde32-112">위치 매개 변수에는 현재 위치 (장애 조치 우선 순위를 기준으로 정렬 됨) 및 새 위치 목록이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="fde32-113">지역만 추가할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="fde32-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="fde32-114">위치 또는 LocationObject 중 하나를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fde32-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="fde32-115">예제의</span><span class="sxs-lookup"><span data-stu-id="fde32-115">EXAMPLES</span></span>

### <span data-ttu-id="fde32-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="fde32-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="fde32-117">변수</span><span class="sxs-lookup"><span data-stu-id="fde32-117">PARAMETERS</span></span>

### <span data-ttu-id="fde32-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fde32-118">-AsJob</span></span>
<span data-ttu-id="fde32-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fde32-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-120">-확인</span><span class="sxs-lookup"><span data-stu-id="fde32-120">-Confirm</span></span>
<span data-ttu-id="fde32-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde32-122">-DefaultProfile</span></span>
<span data-ttu-id="fde32-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde32-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fde32-124">-InputObject</span></span>
<span data-ttu-id="fde32-125">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-126">-위치</span><span class="sxs-lookup"><span data-stu-id="fde32-126">-Location</span></span>
<span data-ttu-id="fde32-127">추가할 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="fde32-128">-LocationObject</span></span>
<span data-ttu-id="fde32-129">Cosmos DB 데이터베이스 계정에 위치를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="fde32-130">PSLocation 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-131">-이름</span><span class="sxs-lookup"><span data-stu-id="fde32-131">-Name</span></span>
<span data-ttu-id="fde32-132">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-132">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde32-133">-ResourceGroupName</span></span>
<span data-ttu-id="fde32-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-134">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fde32-135">-ResourceId</span></span>
<span data-ttu-id="fde32-136">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-136">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde32-137">-WhatIf</span></span>
<span data-ttu-id="fde32-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde32-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde32-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde32-140">CommonParameters</span></span>
<span data-ttu-id="fde32-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde32-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde32-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fde32-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde32-143">입력</span><span class="sxs-lookup"><span data-stu-id="fde32-143">INPUTS</span></span>

### <span data-ttu-id="fde32-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fde32-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fde32-145">출력</span><span class="sxs-lookup"><span data-stu-id="fde32-145">OUTPUTS</span></span>

### <span data-ttu-id="fde32-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fde32-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fde32-147">상속자</span><span class="sxs-lookup"><span data-stu-id="fde32-147">NOTES</span></span>

## <span data-ttu-id="fde32-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fde32-148">RELATED LINKS</span></span>
