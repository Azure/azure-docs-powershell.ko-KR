---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042193"
---
# <span data-ttu-id="1998c-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="1998c-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="1998c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1998c-102">SYNOPSIS</span></span>
<span data-ttu-id="1998c-103">CosmosDB 테이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="1998c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1998c-104">SYNTAX</span></span>

### <span data-ttu-id="1998c-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1998c-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1998c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1998c-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1998c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1998c-107">DESCRIPTION</span></span>
<span data-ttu-id="1998c-108">**AzCosmosDBTable** cmdlet은 기존 테이블을 완전히 대체 하 여 새 테이블을 만들거나 기존 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="1998c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1998c-109">EXAMPLES</span></span>

### <span data-ttu-id="1998c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1998c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="1998c-111">리소스 개체에는 테이블의 _rid, _ts, _ etag 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="1998c-112">변수</span><span class="sxs-lookup"><span data-stu-id="1998c-112">PARAMETERS</span></span>

### <span data-ttu-id="1998c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1998c-113">-AccountName</span></span>
<span data-ttu-id="1998c-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1998c-115">-확인</span><span class="sxs-lookup"><span data-stu-id="1998c-115">-Confirm</span></span>
<span data-ttu-id="1998c-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1998c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1998c-117">-DefaultProfile</span></span>
<span data-ttu-id="1998c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1998c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1998c-119">-InputObject</span></span>
<span data-ttu-id="1998c-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="1998c-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1998c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1998c-121">-Name</span></span>
<span data-ttu-id="1998c-122">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-122">Name of the Table.</span></span>

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

### <span data-ttu-id="1998c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1998c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1998c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-124">Name of resource group.</span></span>

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

### <span data-ttu-id="1998c-125">-처리량</span><span class="sxs-lookup"><span data-stu-id="1998c-125">-Throughput</span></span>
<span data-ttu-id="1998c-126">테이블의 처리량 (1/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="1998c-127">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1998c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1998c-128">-WhatIf</span></span>
<span data-ttu-id="1998c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1998c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1998c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1998c-131">CommonParameters</span></span>
<span data-ttu-id="1998c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1998c-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1998c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1998c-134">입력</span><span class="sxs-lookup"><span data-stu-id="1998c-134">INPUTS</span></span>

### <span data-ttu-id="1998c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1998c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1998c-136">출력</span><span class="sxs-lookup"><span data-stu-id="1998c-136">OUTPUTS</span></span>

### <span data-ttu-id="1998c-137">CosmosDB. PSTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="1998c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="1998c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1998c-138">NOTES</span></span>

## <span data-ttu-id="1998c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1998c-139">RELATED LINKS</span></span>
