---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048376"
---
# <span data-ttu-id="db611-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="db611-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="db611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db611-102">SYNOPSIS</span></span>
<span data-ttu-id="db611-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="db611-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="db611-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db611-104">SYNTAX</span></span>

### <span data-ttu-id="db611-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="db611-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db611-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db611-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db611-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db611-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db611-108">설명은</span><span class="sxs-lookup"><span data-stu-id="db611-108">DESCRIPTION</span></span>
<span data-ttu-id="db611-109">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="db611-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="db611-110">예제의</span><span class="sxs-lookup"><span data-stu-id="db611-110">EXAMPLES</span></span>

### <span data-ttu-id="db611-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="db611-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="db611-112">Failoverpolicies, failoverpolicies 1, region2, Failoverpolicies 2, region3, Failoverpolicies 3으로 차례로 업데이트 됨</span><span class="sxs-lookup"><span data-stu-id="db611-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="db611-113">변수</span><span class="sxs-lookup"><span data-stu-id="db611-113">PARAMETERS</span></span>

### <span data-ttu-id="db611-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db611-114">-AsJob</span></span>
<span data-ttu-id="db611-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="db611-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db611-116">-확인</span><span class="sxs-lookup"><span data-stu-id="db611-116">-Confirm</span></span>
<span data-ttu-id="db611-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db611-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db611-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db611-118">-DefaultProfile</span></span>
<span data-ttu-id="db611-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db611-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db611-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="db611-120">-FailoverPolicy</span></span>
<span data-ttu-id="db611-121">지역 이름이 있는 문자열 배열을 장애 조치 우선 순위로 정렬 했습니다.</span><span class="sxs-lookup"><span data-stu-id="db611-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="db611-122">예: 미국, westus</span><span class="sxs-lookup"><span data-stu-id="db611-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="db611-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db611-123">-InputObject</span></span>
<span data-ttu-id="db611-124">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="db611-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="db611-125">-이름</span><span class="sxs-lookup"><span data-stu-id="db611-125">-Name</span></span>
<span data-ttu-id="db611-126">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db611-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="db611-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db611-127">-ResourceGroupName</span></span>
<span data-ttu-id="db611-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db611-128">Name of resource group.</span></span>

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

### <span data-ttu-id="db611-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db611-129">-ResourceId</span></span>
<span data-ttu-id="db611-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="db611-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="db611-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db611-131">-WhatIf</span></span>
<span data-ttu-id="db611-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db611-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db611-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db611-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db611-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db611-134">CommonParameters</span></span>
<span data-ttu-id="db611-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db611-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db611-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db611-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db611-137">입력</span><span class="sxs-lookup"><span data-stu-id="db611-137">INPUTS</span></span>

### <span data-ttu-id="db611-138">않아야</span><span class="sxs-lookup"><span data-stu-id="db611-138">None</span></span>

## <span data-ttu-id="db611-139">출력</span><span class="sxs-lookup"><span data-stu-id="db611-139">OUTPUTS</span></span>

### <span data-ttu-id="db611-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="db611-140">System.Void</span></span>

## <span data-ttu-id="db611-141">상속자</span><span class="sxs-lookup"><span data-stu-id="db611-141">NOTES</span></span>

## <span data-ttu-id="db611-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db611-142">RELATED LINKS</span></span>
