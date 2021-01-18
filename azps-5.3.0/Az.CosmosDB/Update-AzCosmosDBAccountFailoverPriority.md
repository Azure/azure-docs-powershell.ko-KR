---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495758"
---
# <span data-ttu-id="046d8-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="046d8-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="046d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046d8-102">SYNOPSIS</span></span>
<span data-ttu-id="046d8-103">{{ 동의어 }}에 채우기</span><span class="sxs-lookup"><span data-stu-id="046d8-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="046d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="046d8-104">SYNTAX</span></span>

### <span data-ttu-id="046d8-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="046d8-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046d8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="046d8-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046d8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="046d8-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046d8-108">설명</span><span class="sxs-lookup"><span data-stu-id="046d8-108">DESCRIPTION</span></span>
<span data-ttu-id="046d8-109">{{ 설명 }}에 입력</span><span class="sxs-lookup"><span data-stu-id="046d8-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="046d8-110">예제</span><span class="sxs-lookup"><span data-stu-id="046d8-110">EXAMPLES</span></span>

### <span data-ttu-id="046d8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="046d8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="046d8-112">FailoverPriority 1로 region1, region2를 FailoverPriority 2로, region3으로 장애 조치(FailoverPriority) 3으로 업데이트한 FailoverPolicies입니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="046d8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="046d8-113">PARAMETERS</span></span>

### <span data-ttu-id="046d8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="046d8-114">-AsJob</span></span>
<span data-ttu-id="046d8-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="046d8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="046d8-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="046d8-116">-Confirm</span></span>
<span data-ttu-id="046d8-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046d8-118">-DefaultProfile</span></span>
<span data-ttu-id="046d8-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="046d8-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="046d8-120">-FailoverPolicy</span></span>
<span data-ttu-id="046d8-121">장애 조치 우선 순위에 따라 지역 이름이 있는 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="046d8-122">예: eastus, westus</span><span class="sxs-lookup"><span data-stu-id="046d8-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="046d8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="046d8-123">-InputObject</span></span>
<span data-ttu-id="046d8-124">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="046d8-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="046d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="046d8-125">-Name</span></span>
<span data-ttu-id="046d8-126">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="046d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="046d8-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="046d8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="046d8-129">-ResourceId</span></span>
<span data-ttu-id="046d8-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="046d8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046d8-131">-WhatIf</span></span>
<span data-ttu-id="046d8-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="046d8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046d8-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046d8-134">CommonParameters</span></span>
<span data-ttu-id="046d8-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="046d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046d8-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="046d8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046d8-137">입력</span><span class="sxs-lookup"><span data-stu-id="046d8-137">INPUTS</span></span>

### <span data-ttu-id="046d8-138">없음</span><span class="sxs-lookup"><span data-stu-id="046d8-138">None</span></span>

## <span data-ttu-id="046d8-139">출력</span><span class="sxs-lookup"><span data-stu-id="046d8-139">OUTPUTS</span></span>

### <span data-ttu-id="046d8-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="046d8-140">System.Void</span></span>

## <span data-ttu-id="046d8-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="046d8-141">NOTES</span></span>

## <span data-ttu-id="046d8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="046d8-142">RELATED LINKS</span></span>
