---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043614"
---
# <span data-ttu-id="6f9a4-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6f9a4-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="6f9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9a4-103">CosmosDB Sql 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="6f9a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f9a4-104">SYNTAX</span></span>

### <span data-ttu-id="6f9a4-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9a4-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9a4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9a4-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9a4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f9a4-107">DESCRIPTION</span></span>
<span data-ttu-id="6f9a4-108">**AzCosmosDBSqlDatabase** cmdlet은 지정 된 ResourceGroupName, AccountName 및 DatabaseName에 해당 하는 CosmosDB Sql 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="6f9a4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6f9a4-109">EXAMPLES</span></span>

### <span data-ttu-id="6f9a4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f9a4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="6f9a4-111">변수</span><span class="sxs-lookup"><span data-stu-id="6f9a4-111">PARAMETERS</span></span>

### <span data-ttu-id="6f9a4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f9a4-112">-AccountName</span></span>
<span data-ttu-id="6f9a4-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6f9a4-114">-확인</span><span class="sxs-lookup"><span data-stu-id="6f9a4-114">-Confirm</span></span>
<span data-ttu-id="6f9a4-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9a4-116">-DefaultProfile</span></span>
<span data-ttu-id="6f9a4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f9a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f9a4-118">-InputObject</span></span>
<span data-ttu-id="6f9a4-119">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9a4-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6f9a4-120">-Name</span></span>
<span data-ttu-id="6f9a4-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-121">Database name.</span></span>

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

### <span data-ttu-id="6f9a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f9a4-122">-PassThru</span></span>
<span data-ttu-id="6f9a4-123">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="6f9a4-124">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="6f9a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f9a4-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6f9a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9a4-127">-WhatIf</span></span>
<span data-ttu-id="6f9a4-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9a4-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9a4-130">CommonParameters</span></span>
<span data-ttu-id="6f9a4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9a4-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f9a4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9a4-133">입력</span><span class="sxs-lookup"><span data-stu-id="6f9a4-133">INPUTS</span></span>

### <span data-ttu-id="6f9a4-134">않아야</span><span class="sxs-lookup"><span data-stu-id="6f9a4-134">None</span></span>

## <span data-ttu-id="6f9a4-135">출력</span><span class="sxs-lookup"><span data-stu-id="6f9a4-135">OUTPUTS</span></span>

### <span data-ttu-id="6f9a4-136">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6f9a4-136">System.Void</span></span>

### <span data-ttu-id="6f9a4-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6f9a4-137">System.Boolean</span></span>

## <span data-ttu-id="6f9a4-138">상속자</span><span class="sxs-lookup"><span data-stu-id="6f9a4-138">NOTES</span></span>

## <span data-ttu-id="6f9a4-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f9a4-139">RELATED LINKS</span></span>
