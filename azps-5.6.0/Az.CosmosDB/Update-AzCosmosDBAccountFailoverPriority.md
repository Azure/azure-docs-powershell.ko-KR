---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 2d3555d879d05e1235fb8713e75c9b27fca46b51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010683"
---
# <span data-ttu-id="93830-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="93830-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="93830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93830-102">SYNOPSIS</span></span>
<span data-ttu-id="93830-103">{{ Synopsis }} 채우기</span><span class="sxs-lookup"><span data-stu-id="93830-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="93830-104">구문</span><span class="sxs-lookup"><span data-stu-id="93830-104">SYNTAX</span></span>

### <span data-ttu-id="93830-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="93830-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93830-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93830-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93830-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93830-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93830-108">설명</span><span class="sxs-lookup"><span data-stu-id="93830-108">DESCRIPTION</span></span>
<span data-ttu-id="93830-109">{{ 설명 }} 채우기</span><span class="sxs-lookup"><span data-stu-id="93830-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="93830-110">예제</span><span class="sxs-lookup"><span data-stu-id="93830-110">EXAMPLES</span></span>

### <span data-ttu-id="93830-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="93830-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="93830-112">FailoverPriority 1, region2를 FailoverPriority 2로 업데이트하고 지역 3을 FailoverPriority 3으로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="93830-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="93830-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="93830-113">PARAMETERS</span></span>

### <span data-ttu-id="93830-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93830-114">-AsJob</span></span>
<span data-ttu-id="93830-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="93830-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93830-116">-확인</span><span class="sxs-lookup"><span data-stu-id="93830-116">-Confirm</span></span>
<span data-ttu-id="93830-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93830-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93830-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93830-118">-DefaultProfile</span></span>
<span data-ttu-id="93830-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93830-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93830-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="93830-120">-FailoverPolicy</span></span>
<span data-ttu-id="93830-121">장애 조치(failover) 우선 순위로 순서가 지정된 지역 이름을 갖는 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="93830-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="93830-122">예: eastus, westus</span><span class="sxs-lookup"><span data-stu-id="93830-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93830-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93830-123">-InputObject</span></span>
<span data-ttu-id="93830-124">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="93830-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="93830-125">-Name</span><span class="sxs-lookup"><span data-stu-id="93830-125">-Name</span></span>
<span data-ttu-id="93830-126">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93830-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="93830-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93830-127">-ResourceGroupName</span></span>
<span data-ttu-id="93830-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93830-128">Name of resource group.</span></span>

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

### <span data-ttu-id="93830-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93830-129">-ResourceId</span></span>
<span data-ttu-id="93830-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="93830-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="93830-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93830-131">-WhatIf</span></span>
<span data-ttu-id="93830-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="93830-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93830-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93830-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93830-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93830-134">CommonParameters</span></span>
<span data-ttu-id="93830-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93830-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93830-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93830-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93830-137">입력</span><span class="sxs-lookup"><span data-stu-id="93830-137">INPUTS</span></span>

### <span data-ttu-id="93830-138">없음</span><span class="sxs-lookup"><span data-stu-id="93830-138">None</span></span>

## <span data-ttu-id="93830-139">출력</span><span class="sxs-lookup"><span data-stu-id="93830-139">OUTPUTS</span></span>

### <span data-ttu-id="93830-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="93830-140">System.Void</span></span>

## <span data-ttu-id="93830-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93830-141">NOTES</span></span>

## <span data-ttu-id="93830-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93830-142">RELATED LINKS</span></span>
