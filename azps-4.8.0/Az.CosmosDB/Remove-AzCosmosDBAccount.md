---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212859"
---
# <span data-ttu-id="29901-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="29901-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="29901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29901-102">SYNOPSIS</span></span>
<span data-ttu-id="29901-103">CosmosDB 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="29901-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="29901-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29901-104">SYNTAX</span></span>

### <span data-ttu-id="29901-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="29901-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29901-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29901-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29901-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29901-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29901-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29901-108">DESCRIPTION</span></span>
<span data-ttu-id="29901-109">지정 된 ResourceGroup에서 주어진 이름으로 CosmosDB 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="29901-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="29901-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29901-110">EXAMPLES</span></span>

### <span data-ttu-id="29901-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="29901-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="29901-112">ResourceGroup rg에서 계정 이름 dbname이 있는 계정이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29901-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="29901-113">변수</span><span class="sxs-lookup"><span data-stu-id="29901-113">PARAMETERS</span></span>

### <span data-ttu-id="29901-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29901-114">-AsJob</span></span>
<span data-ttu-id="29901-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="29901-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29901-116">-확인</span><span class="sxs-lookup"><span data-stu-id="29901-116">-Confirm</span></span>
<span data-ttu-id="29901-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29901-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29901-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29901-118">-DefaultProfile</span></span>
<span data-ttu-id="29901-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29901-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29901-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29901-120">-InputObject</span></span>
<span data-ttu-id="29901-121">데이터베이스 계정 개체</span><span class="sxs-lookup"><span data-stu-id="29901-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29901-122">-이름</span><span class="sxs-lookup"><span data-stu-id="29901-122">-Name</span></span>
<span data-ttu-id="29901-123">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29901-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="29901-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29901-124">-PassThru</span></span>
<span data-ttu-id="29901-125">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29901-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="29901-126">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="29901-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="29901-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29901-127">-ResourceGroupName</span></span>
<span data-ttu-id="29901-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29901-128">Name of resource group.</span></span>

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

### <span data-ttu-id="29901-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29901-129">-ResourceId</span></span>
<span data-ttu-id="29901-130">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="29901-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="29901-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29901-131">-WhatIf</span></span>
<span data-ttu-id="29901-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29901-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29901-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29901-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29901-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29901-134">CommonParameters</span></span>
<span data-ttu-id="29901-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29901-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29901-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29901-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29901-137">입력</span><span class="sxs-lookup"><span data-stu-id="29901-137">INPUTS</span></span>

### <span data-ttu-id="29901-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="29901-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="29901-139">출력</span><span class="sxs-lookup"><span data-stu-id="29901-139">OUTPUTS</span></span>

### <span data-ttu-id="29901-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="29901-140">System.Void</span></span>

## <span data-ttu-id="29901-141">상속자</span><span class="sxs-lookup"><span data-stu-id="29901-141">NOTES</span></span>

## <span data-ttu-id="29901-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29901-142">RELATED LINKS</span></span>
