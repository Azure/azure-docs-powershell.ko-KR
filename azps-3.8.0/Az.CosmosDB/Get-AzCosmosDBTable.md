---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044882"
---
# <span data-ttu-id="91732-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="91732-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="91732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91732-102">SYNOPSIS</span></span>
<span data-ttu-id="91732-103">CosmosDB 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91732-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="91732-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91732-104">SYNTAX</span></span>

### <span data-ttu-id="91732-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="91732-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91732-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91732-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91732-107">설명은</span><span class="sxs-lookup"><span data-stu-id="91732-107">DESCRIPTION</span></span>
<span data-ttu-id="91732-108">**Get-AzCosmosDBTable** cmdlet은 기존 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91732-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="91732-109">예제의</span><span class="sxs-lookup"><span data-stu-id="91732-109">EXAMPLES</span></span>

### <span data-ttu-id="91732-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="91732-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="91732-111">리소스 개체에는 테이블의 _rid, _ts, _ etag 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91732-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="91732-112">변수</span><span class="sxs-lookup"><span data-stu-id="91732-112">PARAMETERS</span></span>

### <span data-ttu-id="91732-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91732-113">-AccountName</span></span>
<span data-ttu-id="91732-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91732-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="91732-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91732-115">-DefaultProfile</span></span>
<span data-ttu-id="91732-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91732-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91732-117">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="91732-117">-Detailed</span></span>
<span data-ttu-id="91732-118">그런 다음 cmdlet은 해당 처리 값이 지정 된 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91732-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="91732-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91732-119">-InputObject</span></span>
<span data-ttu-id="91732-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="91732-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91732-121">-이름</span><span class="sxs-lookup"><span data-stu-id="91732-121">-Name</span></span>
<span data-ttu-id="91732-122">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91732-122">Name of the Table.</span></span>

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

### <span data-ttu-id="91732-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91732-123">-ResourceGroupName</span></span>
<span data-ttu-id="91732-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91732-124">Name of resource group.</span></span>

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

### <span data-ttu-id="91732-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91732-125">CommonParameters</span></span>
<span data-ttu-id="91732-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91732-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91732-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91732-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91732-128">입력</span><span class="sxs-lookup"><span data-stu-id="91732-128">INPUTS</span></span>

### <span data-ttu-id="91732-129">않아야</span><span class="sxs-lookup"><span data-stu-id="91732-129">None</span></span>

## <span data-ttu-id="91732-130">출력</span><span class="sxs-lookup"><span data-stu-id="91732-130">OUTPUTS</span></span>

### <span data-ttu-id="91732-131">CosmosDB. PSTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="91732-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="91732-132">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="91732-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="91732-133">상속자</span><span class="sxs-lookup"><span data-stu-id="91732-133">NOTES</span></span>

## <span data-ttu-id="91732-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91732-134">RELATED LINKS</span></span>
