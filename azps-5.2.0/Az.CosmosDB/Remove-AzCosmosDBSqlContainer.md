---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351561"
---
# <span data-ttu-id="0afb9-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="0afb9-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="0afb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afb9-102">SYNOPSIS</span></span>
<span data-ttu-id="0afb9-103">CosmosDB Sql 컨테이너를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0afb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="0afb9-104">SYNTAX</span></span>

### <span data-ttu-id="0afb9-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0afb9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afb9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0afb9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afb9-107">설명</span><span class="sxs-lookup"><span data-stu-id="0afb9-107">DESCRIPTION</span></span>
<span data-ttu-id="0afb9-108">**Remove-AzCosmosDBSqlContainer** cmdlet은 주어진 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 해당하는 CosmosDB Sql 컨테이너를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="0afb9-109">예제</span><span class="sxs-lookup"><span data-stu-id="0afb9-109">EXAMPLES</span></span>

### <span data-ttu-id="0afb9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0afb9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="0afb9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afb9-111">PARAMETERS</span></span>

### <span data-ttu-id="0afb9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0afb9-112">-AccountName</span></span>
<span data-ttu-id="0afb9-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0afb9-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0afb9-114">-Confirm</span></span>
<span data-ttu-id="0afb9-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afb9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0afb9-116">-DatabaseName</span></span>
<span data-ttu-id="0afb9-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-117">Database name.</span></span>

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

### <span data-ttu-id="0afb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afb9-118">-DefaultProfile</span></span>
<span data-ttu-id="0afb9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afb9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0afb9-120">-InputObject</span></span>
<span data-ttu-id="0afb9-121">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0afb9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0afb9-122">-Name</span></span>
<span data-ttu-id="0afb9-123">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-123">Container name.</span></span>

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

### <span data-ttu-id="0afb9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0afb9-124">-PassThru</span></span>
<span data-ttu-id="0afb9-125">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="0afb9-126">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="0afb9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afb9-127">-ResourceGroupName</span></span>
<span data-ttu-id="0afb9-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-128">Name of resource group.</span></span>

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

### <span data-ttu-id="0afb9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afb9-129">-WhatIf</span></span>
<span data-ttu-id="0afb9-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0afb9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afb9-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afb9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afb9-132">CommonParameters</span></span>
<span data-ttu-id="0afb9-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0afb9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afb9-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0afb9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afb9-135">입력</span><span class="sxs-lookup"><span data-stu-id="0afb9-135">INPUTS</span></span>

### <span data-ttu-id="0afb9-136">없음</span><span class="sxs-lookup"><span data-stu-id="0afb9-136">None</span></span>

## <span data-ttu-id="0afb9-137">출력</span><span class="sxs-lookup"><span data-stu-id="0afb9-137">OUTPUTS</span></span>

### <span data-ttu-id="0afb9-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="0afb9-138">System.Void</span></span>

### <span data-ttu-id="0afb9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0afb9-139">System.Boolean</span></span>

## <span data-ttu-id="0afb9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0afb9-140">NOTES</span></span>

## <span data-ttu-id="0afb9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0afb9-141">RELATED LINKS</span></span>