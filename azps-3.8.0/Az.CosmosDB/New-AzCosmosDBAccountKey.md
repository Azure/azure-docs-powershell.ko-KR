---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041917"
---
# <span data-ttu-id="6ed23-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ed23-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="6ed23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed23-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed23-103">지정 된 CosmosDB Account 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="6ed23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ed23-104">SYNTAX</span></span>

### <span data-ttu-id="6ed23-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ed23-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed23-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ed23-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed23-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ed23-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ed23-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ed23-108">DESCRIPTION</span></span>
<span data-ttu-id="6ed23-109">지정 된 ResourceGroup에 새 CosmosDB Account를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="6ed23-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ed23-110">EXAMPLES</span></span>

### <span data-ttu-id="6ed23-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ed23-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="6ed23-112">ResourceGroup rg에서 계정 이름 dbname을 사용 하는 계정에 대해 새 키가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="6ed23-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ed23-113">PARAMETERS</span></span>

### <span data-ttu-id="6ed23-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ed23-114">-AsJob</span></span>
<span data-ttu-id="6ed23-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ed23-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ed23-116">-확인</span><span class="sxs-lookup"><span data-stu-id="6ed23-116">-Confirm</span></span>
<span data-ttu-id="6ed23-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed23-118">-DefaultProfile</span></span>
<span data-ttu-id="6ed23-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ed23-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ed23-120">-InputObject</span></span>
<span data-ttu-id="6ed23-121">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="6ed23-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed23-122">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="6ed23-122">-KeyKind</span></span>
<span data-ttu-id="6ed23-123">다시 생성할 선택 키입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-123">The access key to regenerate.</span></span>
<span data-ttu-id="6ed23-124">허용 되는 값: 기본, primaryReadonly, secondary, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="6ed23-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

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

### <span data-ttu-id="6ed23-125">-이름</span><span class="sxs-lookup"><span data-stu-id="6ed23-125">-Name</span></span>
<span data-ttu-id="6ed23-126">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6ed23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed23-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ed23-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6ed23-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ed23-129">-ResourceId</span></span>
<span data-ttu-id="6ed23-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed23-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed23-131">-WhatIf</span></span>
<span data-ttu-id="6ed23-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ed23-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed23-134">CommonParameters</span></span>
<span data-ttu-id="6ed23-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed23-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ed23-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed23-137">입력</span><span class="sxs-lookup"><span data-stu-id="6ed23-137">INPUTS</span></span>

### <span data-ttu-id="6ed23-138">않아야</span><span class="sxs-lookup"><span data-stu-id="6ed23-138">None</span></span>

## <span data-ttu-id="6ed23-139">출력</span><span class="sxs-lookup"><span data-stu-id="6ed23-139">OUTPUTS</span></span>

### <span data-ttu-id="6ed23-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6ed23-140">System.Void</span></span>

## <span data-ttu-id="6ed23-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6ed23-141">NOTES</span></span>

## <span data-ttu-id="6ed23-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ed23-142">RELATED LINKS</span></span>
