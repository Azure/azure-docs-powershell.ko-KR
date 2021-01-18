---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493722"
---
# <span data-ttu-id="fbefa-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="fbefa-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="fbefa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbefa-102">SYNOPSIS</span></span>
<span data-ttu-id="fbefa-103">CosmosDB 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="fbefa-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbefa-104">SYNTAX</span></span>

### <span data-ttu-id="fbefa-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fbefa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbefa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbefa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbefa-107">설명</span><span class="sxs-lookup"><span data-stu-id="fbefa-107">DESCRIPTION</span></span>
<span data-ttu-id="fbefa-108">**Get-AzCosmosDBTable** cmdlet은 기존 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="fbefa-109">예제</span><span class="sxs-lookup"><span data-stu-id="fbefa-109">EXAMPLES</span></span>

### <span data-ttu-id="fbefa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbefa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="fbefa-111">리소스 개체에는 _rid, _ts, _ etag 속성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="fbefa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbefa-112">PARAMETERS</span></span>

### <span data-ttu-id="fbefa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fbefa-113">-AccountName</span></span>
<span data-ttu-id="fbefa-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fbefa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbefa-115">-DefaultProfile</span></span>
<span data-ttu-id="fbefa-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbefa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fbefa-117">-Name</span></span>
<span data-ttu-id="fbefa-118">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-118">Name of the Table.</span></span>

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

### <span data-ttu-id="fbefa-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fbefa-119">-ParentObject</span></span>
<span data-ttu-id="fbefa-120">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="fbefa-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fbefa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbefa-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbefa-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-122">Name of resource group.</span></span>

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

### <span data-ttu-id="fbefa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbefa-123">CommonParameters</span></span>
<span data-ttu-id="fbefa-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbefa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbefa-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbefa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbefa-126">입력</span><span class="sxs-lookup"><span data-stu-id="fbefa-126">INPUTS</span></span>

### <span data-ttu-id="fbefa-127">없음</span><span class="sxs-lookup"><span data-stu-id="fbefa-127">None</span></span>

## <span data-ttu-id="fbefa-128">출력</span><span class="sxs-lookup"><span data-stu-id="fbefa-128">OUTPUTS</span></span>

### <span data-ttu-id="fbefa-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fbefa-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="fbefa-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fbefa-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fbefa-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbefa-131">NOTES</span></span>

## <span data-ttu-id="fbefa-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbefa-132">RELATED LINKS</span></span>
