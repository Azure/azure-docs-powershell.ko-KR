---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212390"
---
# <span data-ttu-id="5fd54-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="5fd54-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="5fd54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fd54-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd54-103">CosmosDB 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="5fd54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5fd54-104">SYNTAX</span></span>

### <span data-ttu-id="5fd54-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5fd54-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fd54-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fd54-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fd54-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5fd54-107">DESCRIPTION</span></span>
<span data-ttu-id="5fd54-108">**Get-AzCosmosDBTable** cmdlet은 기존 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="5fd54-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5fd54-109">EXAMPLES</span></span>

### <span data-ttu-id="5fd54-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5fd54-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="5fd54-111">리소스 개체에는 테이블의 _rid, _ts, _ etag 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="5fd54-112">변수</span><span class="sxs-lookup"><span data-stu-id="5fd54-112">PARAMETERS</span></span>

### <span data-ttu-id="5fd54-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5fd54-113">-AccountName</span></span>
<span data-ttu-id="5fd54-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5fd54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd54-115">-DefaultProfile</span></span>
<span data-ttu-id="5fd54-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd54-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5fd54-117">-Name</span></span>
<span data-ttu-id="5fd54-118">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-118">Name of the Table.</span></span>

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

### <span data-ttu-id="5fd54-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5fd54-119">-ParentObject</span></span>
<span data-ttu-id="5fd54-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="5fd54-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd54-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd54-121">-ResourceGroupName</span></span>
<span data-ttu-id="5fd54-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-122">Name of resource group.</span></span>

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

### <span data-ttu-id="5fd54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd54-123">CommonParameters</span></span>
<span data-ttu-id="5fd54-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd54-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5fd54-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd54-126">입력</span><span class="sxs-lookup"><span data-stu-id="5fd54-126">INPUTS</span></span>

### <span data-ttu-id="5fd54-127">않아야</span><span class="sxs-lookup"><span data-stu-id="5fd54-127">None</span></span>

## <span data-ttu-id="5fd54-128">출력</span><span class="sxs-lookup"><span data-stu-id="5fd54-128">OUTPUTS</span></span>

### <span data-ttu-id="5fd54-129">CosmosDB. PSTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="5fd54-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="5fd54-130">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="5fd54-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5fd54-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5fd54-131">NOTES</span></span>

## <span data-ttu-id="5fd54-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fd54-132">RELATED LINKS</span></span>
