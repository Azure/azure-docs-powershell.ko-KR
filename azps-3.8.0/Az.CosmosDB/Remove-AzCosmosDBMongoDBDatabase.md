---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043617"
---
# <span data-ttu-id="92b59-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="92b59-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="92b59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b59-102">SYNOPSIS</span></span>
<span data-ttu-id="92b59-103">CosmosDB MongoDB 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="92b59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92b59-104">SYNTAX</span></span>

### <span data-ttu-id="92b59-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92b59-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b59-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92b59-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b59-107">설명은</span><span class="sxs-lookup"><span data-stu-id="92b59-107">DESCRIPTION</span></span>
<span data-ttu-id="92b59-108">**AzCosmosDBMongoDBDatabase** Cmdlet은 CosmosDB MongoDB 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="92b59-109">예제의</span><span class="sxs-lookup"><span data-stu-id="92b59-109">EXAMPLES</span></span>

### <span data-ttu-id="92b59-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="92b59-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="92b59-111">Cmdlet은 삭제가 성공한 경우 true 인 bool (-PassThru가 전달 되는 경우) 형식의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="92b59-112">변수</span><span class="sxs-lookup"><span data-stu-id="92b59-112">PARAMETERS</span></span>

### <span data-ttu-id="92b59-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92b59-113">-AccountName</span></span>
<span data-ttu-id="92b59-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="92b59-115">-확인</span><span class="sxs-lookup"><span data-stu-id="92b59-115">-Confirm</span></span>
<span data-ttu-id="92b59-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b59-117">-DefaultProfile</span></span>
<span data-ttu-id="92b59-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b59-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b59-119">-InputObject</span></span>
<span data-ttu-id="92b59-120">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92b59-121">-이름</span><span class="sxs-lookup"><span data-stu-id="92b59-121">-Name</span></span>
<span data-ttu-id="92b59-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-122">Database name.</span></span>

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

### <span data-ttu-id="92b59-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b59-123">-PassThru</span></span>
<span data-ttu-id="92b59-124">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="92b59-125">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="92b59-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b59-126">-ResourceGroupName</span></span>
<span data-ttu-id="92b59-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-127">Name of resource group.</span></span>

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

### <span data-ttu-id="92b59-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b59-128">-WhatIf</span></span>
<span data-ttu-id="92b59-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b59-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b59-131">CommonParameters</span></span>
<span data-ttu-id="92b59-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b59-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="92b59-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b59-134">입력</span><span class="sxs-lookup"><span data-stu-id="92b59-134">INPUTS</span></span>

### <span data-ttu-id="92b59-135">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="92b59-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="92b59-136">출력</span><span class="sxs-lookup"><span data-stu-id="92b59-136">OUTPUTS</span></span>

### <span data-ttu-id="92b59-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="92b59-137">System.Void</span></span>

### <span data-ttu-id="92b59-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="92b59-138">System.Boolean</span></span>

## <span data-ttu-id="92b59-139">상속자</span><span class="sxs-lookup"><span data-stu-id="92b59-139">NOTES</span></span>

## <span data-ttu-id="92b59-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92b59-140">RELATED LINKS</span></span>
