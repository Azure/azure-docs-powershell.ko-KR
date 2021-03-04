---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: d860e9f5992cb1bd8df9a3f7f14e51565412284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975904"
---
# <span data-ttu-id="4dddf-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="4dddf-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="4dddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dddf-102">SYNOPSIS</span></span>
<span data-ttu-id="4dddf-103">CosmosDB Cassandra Table을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4dddf-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dddf-104">SYNTAX</span></span>

### <span data-ttu-id="4dddf-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4dddf-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dddf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dddf-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dddf-107">설명</span><span class="sxs-lookup"><span data-stu-id="4dddf-107">DESCRIPTION</span></span>
<span data-ttu-id="4dddf-108">**Remove-AzCosmosDBCasandraTable은** CosmosDB Cassandra 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4dddf-109">예제</span><span class="sxs-lookup"><span data-stu-id="4dddf-109">EXAMPLES</span></span>

### <span data-ttu-id="4dddf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4dddf-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="4dddf-111">cmdlet은 삭제가 성공한 경우 true인 형식 bool(-PassThru가 전달될 때)의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="4dddf-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dddf-112">PARAMETERS</span></span>

### <span data-ttu-id="4dddf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4dddf-113">-AccountName</span></span>
<span data-ttu-id="4dddf-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4dddf-115">-확인</span><span class="sxs-lookup"><span data-stu-id="4dddf-115">-Confirm</span></span>
<span data-ttu-id="4dddf-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dddf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dddf-117">-DefaultProfile</span></span>
<span data-ttu-id="4dddf-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dddf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dddf-119">-InputObject</span></span>
<span data-ttu-id="4dddf-120">Cassandra Table 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dddf-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="4dddf-121">-KeyspaceName</span></span>
<span data-ttu-id="4dddf-122">Cassandra 키스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4dddf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4dddf-123">-Name</span></span>
<span data-ttu-id="4dddf-124">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4dddf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dddf-125">-PassThru</span></span>
<span data-ttu-id="4dddf-126">사용자가 출력을 수신하려는 경우 true로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4dddf-127">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4dddf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dddf-128">-ResourceGroupName</span></span>
<span data-ttu-id="4dddf-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4dddf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dddf-130">-WhatIf</span></span>
<span data-ttu-id="4dddf-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dddf-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dddf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dddf-133">CommonParameters</span></span>
<span data-ttu-id="4dddf-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dddf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dddf-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dddf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dddf-136">입력</span><span class="sxs-lookup"><span data-stu-id="4dddf-136">INPUTS</span></span>

### <span data-ttu-id="4dddf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4dddf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="4dddf-138">출력</span><span class="sxs-lookup"><span data-stu-id="4dddf-138">OUTPUTS</span></span>

### <span data-ttu-id="4dddf-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="4dddf-139">System.Void</span></span>

### <span data-ttu-id="4dddf-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dddf-140">System.Boolean</span></span>

## <span data-ttu-id="4dddf-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dddf-141">NOTES</span></span>

## <span data-ttu-id="4dddf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dddf-142">RELATED LINKS</span></span>
