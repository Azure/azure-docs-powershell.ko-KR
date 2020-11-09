---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306866"
---
# <span data-ttu-id="8af05-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="8af05-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="8af05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af05-102">SYNOPSIS</span></span>
<span data-ttu-id="8af05-103">CosmosDB Sql UserDefinedFunction를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="8af05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8af05-104">SYNTAX</span></span>

### <span data-ttu-id="8af05-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8af05-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af05-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8af05-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af05-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8af05-107">DESCRIPTION</span></span>
<span data-ttu-id="8af05-108">**AzCosmosDBSqlUserDefinedFunction** cmdlet은 지정 된 ResourceGroupName, AccountName 및 DatabaseName에 해당 하는 CosmosDB Sql UserDefinedFunction을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="8af05-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8af05-109">EXAMPLES</span></span>

### <span data-ttu-id="8af05-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8af05-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="8af05-111">변수</span><span class="sxs-lookup"><span data-stu-id="8af05-111">PARAMETERS</span></span>

### <span data-ttu-id="8af05-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8af05-112">-AccountName</span></span>
<span data-ttu-id="8af05-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8af05-114">-확인</span><span class="sxs-lookup"><span data-stu-id="8af05-114">-Confirm</span></span>
<span data-ttu-id="8af05-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af05-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8af05-116">-ContainerName</span></span>
<span data-ttu-id="8af05-117">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-117">Container name.</span></span>

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

### <span data-ttu-id="8af05-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8af05-118">-DatabaseName</span></span>
<span data-ttu-id="8af05-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-119">Database name.</span></span>

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

### <span data-ttu-id="8af05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af05-120">-DefaultProfile</span></span>
<span data-ttu-id="8af05-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af05-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8af05-122">-InputObject</span></span>
<span data-ttu-id="8af05-123">Sql 사용자 정의 함수 개체</span><span class="sxs-lookup"><span data-stu-id="8af05-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8af05-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8af05-124">-Name</span></span>
<span data-ttu-id="8af05-125">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="8af05-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8af05-126">-PassThru</span></span>
<span data-ttu-id="8af05-127">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="8af05-128">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="8af05-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af05-129">-ResourceGroupName</span></span>
<span data-ttu-id="8af05-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-130">Name of resource group.</span></span>

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

### <span data-ttu-id="8af05-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af05-131">-WhatIf</span></span>
<span data-ttu-id="8af05-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af05-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af05-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af05-134">CommonParameters</span></span>
<span data-ttu-id="8af05-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af05-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af05-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8af05-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af05-137">입력</span><span class="sxs-lookup"><span data-stu-id="8af05-137">INPUTS</span></span>

### <span data-ttu-id="8af05-138">않아야</span><span class="sxs-lookup"><span data-stu-id="8af05-138">None</span></span>

## <span data-ttu-id="8af05-139">출력</span><span class="sxs-lookup"><span data-stu-id="8af05-139">OUTPUTS</span></span>

### <span data-ttu-id="8af05-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="8af05-140">System.Void</span></span>

### <span data-ttu-id="8af05-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8af05-141">System.Boolean</span></span>

## <span data-ttu-id="8af05-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8af05-142">NOTES</span></span>

## <span data-ttu-id="8af05-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8af05-143">RELATED LINKS</span></span>
