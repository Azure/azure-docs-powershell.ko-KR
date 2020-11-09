---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307220"
---
# <span data-ttu-id="6cebf-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="6cebf-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="6cebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cebf-102">SYNOPSIS</span></span>
<span data-ttu-id="6cebf-103">CosmosDB 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="6cebf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cebf-104">SYNTAX</span></span>

### <span data-ttu-id="6cebf-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6cebf-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cebf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cebf-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cebf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6cebf-107">DESCRIPTION</span></span>
<span data-ttu-id="6cebf-108">**Get-AzCosmosDBTable** cmdlet은 기존 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="6cebf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6cebf-109">EXAMPLES</span></span>

### <span data-ttu-id="6cebf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6cebf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="6cebf-111">리소스 개체에는 테이블의 _rid, _ts, _ etag 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="6cebf-112">변수</span><span class="sxs-lookup"><span data-stu-id="6cebf-112">PARAMETERS</span></span>

### <span data-ttu-id="6cebf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6cebf-113">-AccountName</span></span>
<span data-ttu-id="6cebf-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6cebf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cebf-115">-DefaultProfile</span></span>
<span data-ttu-id="6cebf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cebf-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6cebf-117">-Name</span></span>
<span data-ttu-id="6cebf-118">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-118">Name of the Table.</span></span>

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

### <span data-ttu-id="6cebf-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6cebf-119">-ParentObject</span></span>
<span data-ttu-id="6cebf-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="6cebf-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6cebf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cebf-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cebf-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-122">Name of resource group.</span></span>

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

### <span data-ttu-id="6cebf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cebf-123">CommonParameters</span></span>
<span data-ttu-id="6cebf-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cebf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cebf-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6cebf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cebf-126">입력</span><span class="sxs-lookup"><span data-stu-id="6cebf-126">INPUTS</span></span>

### <span data-ttu-id="6cebf-127">않아야</span><span class="sxs-lookup"><span data-stu-id="6cebf-127">None</span></span>

## <span data-ttu-id="6cebf-128">출력</span><span class="sxs-lookup"><span data-stu-id="6cebf-128">OUTPUTS</span></span>

### <span data-ttu-id="6cebf-129">CosmosDB. PSTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6cebf-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="6cebf-130">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6cebf-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6cebf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="6cebf-131">NOTES</span></span>

## <span data-ttu-id="6cebf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cebf-132">RELATED LINKS</span></span>
