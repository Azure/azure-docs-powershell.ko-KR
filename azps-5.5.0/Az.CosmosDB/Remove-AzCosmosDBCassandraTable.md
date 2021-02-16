---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198945"
---
# <span data-ttu-id="706b5-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="706b5-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="706b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="706b5-102">SYNOPSIS</span></span>
<span data-ttu-id="706b5-103">CosmosDB Cassandra 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="706b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="706b5-104">SYNTAX</span></span>

### <span data-ttu-id="706b5-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="706b5-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="706b5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="706b5-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="706b5-107">설명</span><span class="sxs-lookup"><span data-stu-id="706b5-107">DESCRIPTION</span></span>
<span data-ttu-id="706b5-108">**Remove-AzCosmosDBCassandraTable은** CosmosDB Cassandra 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="706b5-109">예제</span><span class="sxs-lookup"><span data-stu-id="706b5-109">EXAMPLES</span></span>

### <span data-ttu-id="706b5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="706b5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="706b5-111">cmdlet은 삭제에 성공한 경우 true인 bool 형식의 개체를 반환합니다(-PassThru가 전달된 경우).</span><span class="sxs-lookup"><span data-stu-id="706b5-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="706b5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="706b5-112">PARAMETERS</span></span>

### <span data-ttu-id="706b5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="706b5-113">-AccountName</span></span>
<span data-ttu-id="706b5-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="706b5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="706b5-115">-Confirm</span></span>
<span data-ttu-id="706b5-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="706b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706b5-117">-DefaultProfile</span></span>
<span data-ttu-id="706b5-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="706b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="706b5-119">-InputObject</span></span>
<span data-ttu-id="706b5-120">Cassandra Table 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="706b5-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="706b5-121">-KeyspaceName</span></span>
<span data-ttu-id="706b5-122">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="706b5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="706b5-123">-Name</span></span>
<span data-ttu-id="706b5-124">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="706b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="706b5-125">-PassThru</span></span>
<span data-ttu-id="706b5-126">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="706b5-127">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="706b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="706b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="706b5-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-129">Name of resource group.</span></span>

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

### <span data-ttu-id="706b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="706b5-130">-WhatIf</span></span>
<span data-ttu-id="706b5-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="706b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="706b5-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="706b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706b5-133">CommonParameters</span></span>
<span data-ttu-id="706b5-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="706b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706b5-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="706b5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706b5-136">입력</span><span class="sxs-lookup"><span data-stu-id="706b5-136">INPUTS</span></span>

### <span data-ttu-id="706b5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="706b5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="706b5-138">출력</span><span class="sxs-lookup"><span data-stu-id="706b5-138">OUTPUTS</span></span>

### <span data-ttu-id="706b5-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="706b5-139">System.Void</span></span>

### <span data-ttu-id="706b5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="706b5-140">System.Boolean</span></span>

## <span data-ttu-id="706b5-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="706b5-141">NOTES</span></span>

## <span data-ttu-id="706b5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="706b5-142">RELATED LINKS</span></span>
