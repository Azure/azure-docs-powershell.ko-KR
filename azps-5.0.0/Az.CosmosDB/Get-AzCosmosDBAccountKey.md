---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307340"
---
# <span data-ttu-id="0d924-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="0d924-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="0d924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d924-102">SYNOPSIS</span></span>
<span data-ttu-id="0d924-103">지정 된 CosmosDB Account에 대 한 {"ConnectionKeys", "PrimaryReadOnly" 또는 "Keys"} 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="0d924-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d924-104">SYNTAX</span></span>

### <span data-ttu-id="0d924-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d924-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d924-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d924-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d924-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d924-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d924-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0d924-108">DESCRIPTION</span></span>
<span data-ttu-id="0d924-109">연결 키 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="0d924-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0d924-110">EXAMPLES</span></span>

### <span data-ttu-id="0d924-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d924-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="0d924-112">CosmosDB 계정에 대 한 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="0d924-113">키 유형은 ConnectionStrings, Keys, ReadOnlyKeys의 값이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="0d924-114">기본값은 키입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-114">Default is Keys.</span></span>

## <span data-ttu-id="0d924-115">변수</span><span class="sxs-lookup"><span data-stu-id="0d924-115">PARAMETERS</span></span>

### <span data-ttu-id="0d924-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d924-116">-DefaultProfile</span></span>
<span data-ttu-id="0d924-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d924-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d924-118">-InputObject</span></span>
<span data-ttu-id="0d924-119">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="0d924-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0d924-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0d924-120">-Name</span></span>
<span data-ttu-id="0d924-121">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0d924-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d924-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d924-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-123">Name of resource group.</span></span>

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

### <span data-ttu-id="0d924-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d924-124">-ResourceId</span></span>
<span data-ttu-id="0d924-125">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="0d924-126">-Type</span><span class="sxs-lookup"><span data-stu-id="0d924-126">-Type</span></span>
<span data-ttu-id="0d924-127">값은 {ConnectionStrings, Keys, ReadOnlyKeys}입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="0d924-128">기본값은 키입니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-128">Default is Keys.</span></span>

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

### <span data-ttu-id="0d924-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d924-129">CommonParameters</span></span>
<span data-ttu-id="0d924-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d924-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d924-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d924-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d924-132">입력</span><span class="sxs-lookup"><span data-stu-id="0d924-132">INPUTS</span></span>

### <span data-ttu-id="0d924-133">않아야</span><span class="sxs-lookup"><span data-stu-id="0d924-133">None</span></span>

## <span data-ttu-id="0d924-134">출력</span><span class="sxs-lookup"><span data-stu-id="0d924-134">OUTPUTS</span></span>

### <span data-ttu-id="0d924-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0d924-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="0d924-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="0d924-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="0d924-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="0d924-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="0d924-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0d924-138">NOTES</span></span>

## <span data-ttu-id="0d924-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d924-139">RELATED LINKS</span></span>
