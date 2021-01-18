---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495769"
---
# <span data-ttu-id="b822b-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b822b-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b822b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b822b-102">SYNOPSIS</span></span>
<span data-ttu-id="b822b-103">CosmosDB 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="b822b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b822b-104">SYNTAX</span></span>

### <span data-ttu-id="b822b-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b822b-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b822b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b822b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b822b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b822b-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b822b-108">설명</span><span class="sxs-lookup"><span data-stu-id="b822b-108">DESCRIPTION</span></span>
<span data-ttu-id="b822b-109">주어진 ResourceGroup에서 이름이 지정한 CosmosDB 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="b822b-110">예제</span><span class="sxs-lookup"><span data-stu-id="b822b-110">EXAMPLES</span></span>

### <span data-ttu-id="b822b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b822b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="b822b-112">ResourceGroup rg에서 계정 이름 dbname이 있는 계정이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="b822b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b822b-113">PARAMETERS</span></span>

### <span data-ttu-id="b822b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b822b-114">-AsJob</span></span>
<span data-ttu-id="b822b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b822b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b822b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b822b-116">-Confirm</span></span>
<span data-ttu-id="b822b-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b822b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b822b-118">-DefaultProfile</span></span>
<span data-ttu-id="b822b-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b822b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b822b-120">-InputObject</span></span>
<span data-ttu-id="b822b-121">데이터베이스 계정 개체</span><span class="sxs-lookup"><span data-stu-id="b822b-121">The Database Account object</span></span>

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

### <span data-ttu-id="b822b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b822b-122">-Name</span></span>
<span data-ttu-id="b822b-123">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b822b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b822b-124">-PassThru</span></span>
<span data-ttu-id="b822b-125">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b822b-126">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b822b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b822b-127">-ResourceGroupName</span></span>
<span data-ttu-id="b822b-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b822b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b822b-129">-ResourceId</span></span>
<span data-ttu-id="b822b-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b822b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b822b-131">-WhatIf</span></span>
<span data-ttu-id="b822b-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b822b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b822b-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b822b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b822b-134">CommonParameters</span></span>
<span data-ttu-id="b822b-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b822b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b822b-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b822b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b822b-137">입력</span><span class="sxs-lookup"><span data-stu-id="b822b-137">INPUTS</span></span>

### <span data-ttu-id="b822b-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b822b-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b822b-139">출력</span><span class="sxs-lookup"><span data-stu-id="b822b-139">OUTPUTS</span></span>

### <span data-ttu-id="b822b-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b822b-140">System.Void</span></span>

## <span data-ttu-id="b822b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b822b-141">NOTES</span></span>

## <span data-ttu-id="b822b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b822b-142">RELATED LINKS</span></span>
