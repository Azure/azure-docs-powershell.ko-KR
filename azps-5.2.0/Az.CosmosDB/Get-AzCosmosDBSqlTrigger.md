---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372394"
---
# <span data-ttu-id="94af6-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="94af6-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="94af6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94af6-102">SYNOPSIS</span></span>
<span data-ttu-id="94af6-103">CosmosDB Sql 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="94af6-104">구문</span><span class="sxs-lookup"><span data-stu-id="94af6-104">SYNTAX</span></span>

### <span data-ttu-id="94af6-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94af6-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94af6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94af6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94af6-107">설명</span><span class="sxs-lookup"><span data-stu-id="94af6-107">DESCRIPTION</span></span>
<span data-ttu-id="94af6-108">**Get-AzCosmosDBSqlTrigger** cmdlet은 주어진 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 대한 모든 기존 CosmosDB Sql 트리거 목록을 구하고, 주어진 ResourceGroupName, AccountName, DatabaseName, ContainerName 및 TriggerName에 대한 단일 CosmosDB Sql 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="94af6-109">예제</span><span class="sxs-lookup"><span data-stu-id="94af6-109">EXAMPLES</span></span>

### <span data-ttu-id="94af6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="94af6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="94af6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94af6-111">PARAMETERS</span></span>

### <span data-ttu-id="94af6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94af6-112">-AccountName</span></span>
<span data-ttu-id="94af6-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="94af6-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="94af6-114">-ContainerName</span></span>
<span data-ttu-id="94af6-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-115">Container name.</span></span>

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

### <span data-ttu-id="94af6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94af6-116">-DatabaseName</span></span>
<span data-ttu-id="94af6-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-117">Database name.</span></span>

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

### <span data-ttu-id="94af6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94af6-118">-DefaultProfile</span></span>
<span data-ttu-id="94af6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94af6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94af6-120">-Name</span></span>
<span data-ttu-id="94af6-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-121">Trigger name.</span></span>

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

### <span data-ttu-id="94af6-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="94af6-122">-ParentObject</span></span>
<span data-ttu-id="94af6-123">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-123">Sql Container object.</span></span>

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

### <span data-ttu-id="94af6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94af6-124">-ResourceGroupName</span></span>
<span data-ttu-id="94af6-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-125">Name of resource group.</span></span>

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

### <span data-ttu-id="94af6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94af6-126">CommonParameters</span></span>
<span data-ttu-id="94af6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94af6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94af6-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94af6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94af6-129">입력</span><span class="sxs-lookup"><span data-stu-id="94af6-129">INPUTS</span></span>

### <span data-ttu-id="94af6-130">없음</span><span class="sxs-lookup"><span data-stu-id="94af6-130">None</span></span>

## <span data-ttu-id="94af6-131">출력</span><span class="sxs-lookup"><span data-stu-id="94af6-131">OUTPUTS</span></span>

### <span data-ttu-id="94af6-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="94af6-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="94af6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94af6-133">NOTES</span></span>

## <span data-ttu-id="94af6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94af6-134">RELATED LINKS</span></span>
