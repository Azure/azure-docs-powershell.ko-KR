---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043713"
---
# <span data-ttu-id="5bf96-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5bf96-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5bf96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bf96-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf96-103">CosmosDB Cassandra Keyspace를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5bf96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5bf96-104">SYNTAX</span></span>

### <span data-ttu-id="5bf96-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf96-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf96-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf96-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5bf96-107">DESCRIPTION</span></span>
<span data-ttu-id="5bf96-108">**AzCosmosDBCassandraKeyspace** cmdlet은 기존 CosmosDB Cassandra Keyspace를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5bf96-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5bf96-109">EXAMPLES</span></span>

### <span data-ttu-id="5bf96-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bf96-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="5bf96-111">Cmdlet은 삭제에 성공한 경우 true 인 bool (-PassThru가 전달 되는 경우) 형식의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="5bf96-112">변수</span><span class="sxs-lookup"><span data-stu-id="5bf96-112">PARAMETERS</span></span>

### <span data-ttu-id="5bf96-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5bf96-113">-AccountName</span></span>
<span data-ttu-id="5bf96-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5bf96-115">-확인</span><span class="sxs-lookup"><span data-stu-id="5bf96-115">-Confirm</span></span>
<span data-ttu-id="5bf96-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf96-117">-DefaultProfile</span></span>
<span data-ttu-id="5bf96-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf96-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bf96-119">-InputObject</span></span>
<span data-ttu-id="5bf96-120">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf96-121">-이름</span><span class="sxs-lookup"><span data-stu-id="5bf96-121">-Name</span></span>
<span data-ttu-id="5bf96-122">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="5bf96-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5bf96-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bf96-123">-PassThru</span></span>
<span data-ttu-id="5bf96-124">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5bf96-125">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5bf96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf96-126">-ResourceGroupName</span></span>
<span data-ttu-id="5bf96-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-127">Name of resource group.</span></span>

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

### <span data-ttu-id="5bf96-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf96-128">-WhatIf</span></span>
<span data-ttu-id="5bf96-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf96-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf96-131">CommonParameters</span></span>
<span data-ttu-id="5bf96-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf96-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bf96-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf96-134">입력</span><span class="sxs-lookup"><span data-stu-id="5bf96-134">INPUTS</span></span>

### <span data-ttu-id="5bf96-135">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="5bf96-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5bf96-136">출력</span><span class="sxs-lookup"><span data-stu-id="5bf96-136">OUTPUTS</span></span>

### <span data-ttu-id="5bf96-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="5bf96-137">System.Void</span></span>

### <span data-ttu-id="5bf96-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5bf96-138">System.Boolean</span></span>

## <span data-ttu-id="5bf96-139">상속자</span><span class="sxs-lookup"><span data-stu-id="5bf96-139">NOTES</span></span>

## <span data-ttu-id="5bf96-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bf96-140">RELATED LINKS</span></span>
