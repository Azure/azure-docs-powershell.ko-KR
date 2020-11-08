---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043618"
---
# <span data-ttu-id="b73be-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="b73be-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="b73be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b73be-102">SYNOPSIS</span></span>
<span data-ttu-id="b73be-103">CosmosDB Sql 컨테이너를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="b73be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b73be-104">SYNTAX</span></span>

### <span data-ttu-id="b73be-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b73be-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b73be-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b73be-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b73be-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b73be-107">DESCRIPTION</span></span>
<span data-ttu-id="b73be-108">**AzCosmosDBSqlContainer** cmdlet은 지정 된 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 해당 하는 CosmosDB Sql 컨테이너를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="b73be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b73be-109">EXAMPLES</span></span>

### <span data-ttu-id="b73be-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b73be-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="b73be-111">변수</span><span class="sxs-lookup"><span data-stu-id="b73be-111">PARAMETERS</span></span>

### <span data-ttu-id="b73be-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b73be-112">-AccountName</span></span>
<span data-ttu-id="b73be-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b73be-114">-확인</span><span class="sxs-lookup"><span data-stu-id="b73be-114">-Confirm</span></span>
<span data-ttu-id="b73be-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b73be-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b73be-116">-DatabaseName</span></span>
<span data-ttu-id="b73be-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-117">Database name.</span></span>

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

### <span data-ttu-id="b73be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73be-118">-DefaultProfile</span></span>
<span data-ttu-id="b73be-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b73be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b73be-120">-InputObject</span></span>
<span data-ttu-id="b73be-121">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="b73be-121">Sql Container object.</span></span>

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

### <span data-ttu-id="b73be-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b73be-122">-Name</span></span>
<span data-ttu-id="b73be-123">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-123">Container name.</span></span>

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

### <span data-ttu-id="b73be-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b73be-124">-PassThru</span></span>
<span data-ttu-id="b73be-125">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b73be-126">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b73be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73be-127">-ResourceGroupName</span></span>
<span data-ttu-id="b73be-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b73be-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73be-129">-WhatIf</span></span>
<span data-ttu-id="b73be-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b73be-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b73be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73be-132">CommonParameters</span></span>
<span data-ttu-id="b73be-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73be-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b73be-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73be-135">입력</span><span class="sxs-lookup"><span data-stu-id="b73be-135">INPUTS</span></span>

### <span data-ttu-id="b73be-136">않아야</span><span class="sxs-lookup"><span data-stu-id="b73be-136">None</span></span>

## <span data-ttu-id="b73be-137">출력</span><span class="sxs-lookup"><span data-stu-id="b73be-137">OUTPUTS</span></span>

### <span data-ttu-id="b73be-138">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b73be-138">System.Void</span></span>

### <span data-ttu-id="b73be-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b73be-139">System.Boolean</span></span>

## <span data-ttu-id="b73be-140">상속자</span><span class="sxs-lookup"><span data-stu-id="b73be-140">NOTES</span></span>

## <span data-ttu-id="b73be-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b73be-141">RELATED LINKS</span></span>
