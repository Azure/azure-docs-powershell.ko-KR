---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181380"
---
# <span data-ttu-id="09fcb-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="09fcb-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="09fcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="09fcb-103">CosmosDB Sql 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="09fcb-104">구문</span><span class="sxs-lookup"><span data-stu-id="09fcb-104">SYNTAX</span></span>

### <span data-ttu-id="09fcb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09fcb-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09fcb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09fcb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09fcb-107">설명</span><span class="sxs-lookup"><span data-stu-id="09fcb-107">DESCRIPTION</span></span>
<span data-ttu-id="09fcb-108">**Get-AzCosmosDBSqlTrigger** cmdlet은 주어진 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 대한 모든 기존 CosmosDB Sql 트리거 목록을 구하고, 주어진 ResourceGroupName, AccountName, DatabaseName, ContainerName 및 TriggerName에 대한 단일 CosmosDB Sql 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="09fcb-109">예제</span><span class="sxs-lookup"><span data-stu-id="09fcb-109">EXAMPLES</span></span>

### <span data-ttu-id="09fcb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="09fcb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="09fcb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09fcb-111">PARAMETERS</span></span>

### <span data-ttu-id="09fcb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09fcb-112">-AccountName</span></span>
<span data-ttu-id="09fcb-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09fcb-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="09fcb-114">-ContainerName</span></span>
<span data-ttu-id="09fcb-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-115">Container name.</span></span>

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

### <span data-ttu-id="09fcb-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09fcb-116">-DatabaseName</span></span>
<span data-ttu-id="09fcb-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-117">Database name.</span></span>

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

### <span data-ttu-id="09fcb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fcb-118">-DefaultProfile</span></span>
<span data-ttu-id="09fcb-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09fcb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="09fcb-120">-Name</span></span>
<span data-ttu-id="09fcb-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-121">Trigger name.</span></span>

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

### <span data-ttu-id="09fcb-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="09fcb-122">-ParentObject</span></span>
<span data-ttu-id="09fcb-123">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-123">Sql Container object.</span></span>

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

### <span data-ttu-id="09fcb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fcb-124">-ResourceGroupName</span></span>
<span data-ttu-id="09fcb-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="09fcb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fcb-126">CommonParameters</span></span>
<span data-ttu-id="09fcb-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09fcb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fcb-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09fcb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fcb-129">입력</span><span class="sxs-lookup"><span data-stu-id="09fcb-129">INPUTS</span></span>

### <span data-ttu-id="09fcb-130">없음</span><span class="sxs-lookup"><span data-stu-id="09fcb-130">None</span></span>

## <span data-ttu-id="09fcb-131">출력</span><span class="sxs-lookup"><span data-stu-id="09fcb-131">OUTPUTS</span></span>

### <span data-ttu-id="09fcb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="09fcb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="09fcb-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09fcb-133">NOTES</span></span>

## <span data-ttu-id="09fcb-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09fcb-134">RELATED LINKS</span></span>
