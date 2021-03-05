---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986911"
---
# <span data-ttu-id="a954f-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="a954f-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="a954f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a954f-102">SYNOPSIS</span></span>
<span data-ttu-id="a954f-103">CosmosDB Sql Trigger를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a954f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a954f-104">SYNTAX</span></span>

### <span data-ttu-id="a954f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a954f-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a954f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a954f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a954f-107">설명</span><span class="sxs-lookup"><span data-stu-id="a954f-107">DESCRIPTION</span></span>
<span data-ttu-id="a954f-108">**Get-AzCosmosDBSqlTrigger** cmdlet은 주어진 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 대한 모든 기존 CosmosDB Sql Trigger의 목록을 얻게 며, 주어진 ResourceGroupName, AccountName, DatabaseName, ContainerName 및 TriggerName에 대한 단일 CosmosDB Sql Trigger을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="a954f-109">예제</span><span class="sxs-lookup"><span data-stu-id="a954f-109">EXAMPLES</span></span>

### <span data-ttu-id="a954f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a954f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="a954f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a954f-111">PARAMETERS</span></span>

### <span data-ttu-id="a954f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a954f-112">-AccountName</span></span>
<span data-ttu-id="a954f-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a954f-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a954f-114">-ContainerName</span></span>
<span data-ttu-id="a954f-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-115">Container name.</span></span>

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

### <span data-ttu-id="a954f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a954f-116">-DatabaseName</span></span>
<span data-ttu-id="a954f-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-117">Database name.</span></span>

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

### <span data-ttu-id="a954f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a954f-118">-DefaultProfile</span></span>
<span data-ttu-id="a954f-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a954f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a954f-120">-Name</span></span>
<span data-ttu-id="a954f-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-121">Trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a954f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a954f-122">-ParentObject</span></span>
<span data-ttu-id="a954f-123">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-123">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a954f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a954f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a954f-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a954f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a954f-126">CommonParameters</span></span>
<span data-ttu-id="a954f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a954f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a954f-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a954f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a954f-129">입력</span><span class="sxs-lookup"><span data-stu-id="a954f-129">INPUTS</span></span>

### <span data-ttu-id="a954f-130">없음</span><span class="sxs-lookup"><span data-stu-id="a954f-130">None</span></span>

## <span data-ttu-id="a954f-131">출력</span><span class="sxs-lookup"><span data-stu-id="a954f-131">OUTPUTS</span></span>

### <span data-ttu-id="a954f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="a954f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="a954f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a954f-133">NOTES</span></span>

## <span data-ttu-id="a954f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a954f-134">RELATED LINKS</span></span>
