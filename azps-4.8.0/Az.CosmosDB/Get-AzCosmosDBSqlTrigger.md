---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215094"
---
# <span data-ttu-id="a52ff-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="a52ff-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="a52ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a52ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a52ff-103">CosmosDB Sql 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a52ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a52ff-104">SYNTAX</span></span>

### <span data-ttu-id="a52ff-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a52ff-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52ff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a52ff-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a52ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a52ff-108">**AzCosmosDBSqlTrigger** cmdlet은 지정 된 ResourceGroupName, Accountname, Databasename 및 ContainerName에 대 한 기존의 모든 CosmosDB sql 트리거 목록을 가져오고 지정 된 ResourceGroupName, Accountname, Databasename, Containername 및 TriggerName에 대 한 단일 CosmosDB sql 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="a52ff-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a52ff-109">EXAMPLES</span></span>

### <span data-ttu-id="a52ff-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a52ff-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="a52ff-111">변수</span><span class="sxs-lookup"><span data-stu-id="a52ff-111">PARAMETERS</span></span>

### <span data-ttu-id="a52ff-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a52ff-112">-AccountName</span></span>
<span data-ttu-id="a52ff-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a52ff-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a52ff-114">-ContainerName</span></span>
<span data-ttu-id="a52ff-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-115">Container name.</span></span>

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

### <span data-ttu-id="a52ff-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a52ff-116">-DatabaseName</span></span>
<span data-ttu-id="a52ff-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-117">Database name.</span></span>

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

### <span data-ttu-id="a52ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52ff-118">-DefaultProfile</span></span>
<span data-ttu-id="a52ff-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a52ff-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a52ff-120">-Name</span></span>
<span data-ttu-id="a52ff-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-121">Trigger name.</span></span>

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

### <span data-ttu-id="a52ff-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a52ff-122">-ParentObject</span></span>
<span data-ttu-id="a52ff-123">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="a52ff-123">Sql Container object.</span></span>

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

### <span data-ttu-id="a52ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="a52ff-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a52ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52ff-126">CommonParameters</span></span>
<span data-ttu-id="a52ff-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a52ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52ff-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a52ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52ff-129">입력</span><span class="sxs-lookup"><span data-stu-id="a52ff-129">INPUTS</span></span>

### <span data-ttu-id="a52ff-130">않아야</span><span class="sxs-lookup"><span data-stu-id="a52ff-130">None</span></span>

## <span data-ttu-id="a52ff-131">출력</span><span class="sxs-lookup"><span data-stu-id="a52ff-131">OUTPUTS</span></span>

### <span data-ttu-id="a52ff-132">CosmosDB. PSSqlTriggerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="a52ff-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="a52ff-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a52ff-133">NOTES</span></span>

## <span data-ttu-id="a52ff-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a52ff-134">RELATED LINKS</span></span>
