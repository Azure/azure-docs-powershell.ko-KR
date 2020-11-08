---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 9ba9c092f021041f1a56626a79e07b369b694d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034024"
---
# <span data-ttu-id="bffc0-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="bffc0-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="bffc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffc0-102">SYNOPSIS</span></span>
<span data-ttu-id="bffc0-103">CosmosDB Sql 데이터베이스에 해당 하는 처리량 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bffc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bffc0-104">SYNTAX</span></span>

### <span data-ttu-id="bffc0-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bffc0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bffc0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bffc0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bffc0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bffc0-107">DESCRIPTION</span></span>
<span data-ttu-id="bffc0-108">**AzCosmosDBSqlDatabaseThroughput** Cmdlet은 CosmosDB Sql 데이터베이스에 해당 하는 처리량 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bffc0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bffc0-109">EXAMPLES</span></span>

### <span data-ttu-id="bffc0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bffc0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="bffc0-111">변수</span><span class="sxs-lookup"><span data-stu-id="bffc0-111">PARAMETERS</span></span>

### <span data-ttu-id="bffc0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bffc0-112">-AccountName</span></span>
<span data-ttu-id="bffc0-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bffc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffc0-114">-DefaultProfile</span></span>
<span data-ttu-id="bffc0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bffc0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bffc0-116">-InputObject</span></span>
<span data-ttu-id="bffc0-117">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="bffc0-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bffc0-118">-이름</span><span class="sxs-lookup"><span data-stu-id="bffc0-118">-Name</span></span>
<span data-ttu-id="bffc0-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-119">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffc0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bffc0-120">-ResourceGroupName</span></span>
<span data-ttu-id="bffc0-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-121">Name of resource group.</span></span>

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

### <span data-ttu-id="bffc0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffc0-122">CommonParameters</span></span>
<span data-ttu-id="bffc0-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bffc0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffc0-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bffc0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffc0-125">입력</span><span class="sxs-lookup"><span data-stu-id="bffc0-125">INPUTS</span></span>

### <span data-ttu-id="bffc0-126">않아야</span><span class="sxs-lookup"><span data-stu-id="bffc0-126">None</span></span>

## <span data-ttu-id="bffc0-127">출력</span><span class="sxs-lookup"><span data-stu-id="bffc0-127">OUTPUTS</span></span>

### <span data-ttu-id="bffc0-128">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="bffc0-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bffc0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="bffc0-129">NOTES</span></span>

## <span data-ttu-id="bffc0-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bffc0-130">RELATED LINKS</span></span>
