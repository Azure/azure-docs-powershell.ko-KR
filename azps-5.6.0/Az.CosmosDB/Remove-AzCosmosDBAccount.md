---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: 64d6f0bd604e8074d593f20a572768b54ced8a59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960784"
---
# <span data-ttu-id="dd0de-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="dd0de-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="dd0de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd0de-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0de-103">CosmosDB 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="dd0de-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd0de-104">SYNTAX</span></span>

### <span data-ttu-id="dd0de-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dd0de-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd0de-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd0de-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd0de-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd0de-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd0de-108">설명</span><span class="sxs-lookup"><span data-stu-id="dd0de-108">DESCRIPTION</span></span>
<span data-ttu-id="dd0de-109">주어진 ResourceGroup에서 지정한 이름으로 CosmosDB 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="dd0de-110">예제</span><span class="sxs-lookup"><span data-stu-id="dd0de-110">EXAMPLES</span></span>

### <span data-ttu-id="dd0de-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd0de-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="dd0de-112">ResourceGroup rg에서 계정 이름 dbname이 있는 계정이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="dd0de-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dd0de-113">PARAMETERS</span></span>

### <span data-ttu-id="dd0de-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd0de-114">-AsJob</span></span>
<span data-ttu-id="dd0de-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dd0de-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd0de-116">-확인</span><span class="sxs-lookup"><span data-stu-id="dd0de-116">-Confirm</span></span>
<span data-ttu-id="dd0de-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd0de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0de-118">-DefaultProfile</span></span>
<span data-ttu-id="dd0de-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd0de-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd0de-120">-InputObject</span></span>
<span data-ttu-id="dd0de-121">데이터베이스 계정 개체</span><span class="sxs-lookup"><span data-stu-id="dd0de-121">The Database Account object</span></span>

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

### <span data-ttu-id="dd0de-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dd0de-122">-Name</span></span>
<span data-ttu-id="dd0de-123">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dd0de-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd0de-124">-PassThru</span></span>
<span data-ttu-id="dd0de-125">사용자가 출력을 수신하려는 경우 true로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dd0de-126">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dd0de-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0de-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd0de-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-128">Name of resource group.</span></span>

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

### <span data-ttu-id="dd0de-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd0de-129">-ResourceId</span></span>
<span data-ttu-id="dd0de-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="dd0de-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd0de-131">-WhatIf</span></span>
<span data-ttu-id="dd0de-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd0de-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd0de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0de-134">CommonParameters</span></span>
<span data-ttu-id="dd0de-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0de-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd0de-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0de-137">입력</span><span class="sxs-lookup"><span data-stu-id="dd0de-137">INPUTS</span></span>

### <span data-ttu-id="dd0de-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="dd0de-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="dd0de-139">출력</span><span class="sxs-lookup"><span data-stu-id="dd0de-139">OUTPUTS</span></span>

### <span data-ttu-id="dd0de-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="dd0de-140">System.Void</span></span>

## <span data-ttu-id="dd0de-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd0de-141">NOTES</span></span>

## <span data-ttu-id="dd0de-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd0de-142">RELATED LINKS</span></span>
