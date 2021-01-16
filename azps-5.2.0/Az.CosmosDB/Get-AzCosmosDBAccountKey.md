---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351998"
---
# <span data-ttu-id="6c3e7-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="6c3e7-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="6c3e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c3e7-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3e7-103">주어진 CosmosDB 계정에 대한 키{"ConnectionKeys", "PrimaryReadOnly" 또는 "키"}를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="6c3e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c3e7-104">SYNTAX</span></span>

### <span data-ttu-id="6c3e7-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6c3e7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c3e7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c3e7-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3e7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c3e7-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c3e7-108">설명</span><span class="sxs-lookup"><span data-stu-id="6c3e7-108">DESCRIPTION</span></span>
<span data-ttu-id="6c3e7-109">연결 키 목록을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="6c3e7-110">예제</span><span class="sxs-lookup"><span data-stu-id="6c3e7-110">EXAMPLES</span></span>

### <span data-ttu-id="6c3e7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c3e7-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="6c3e7-112">CosmosDB 계정에 대한 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="6c3e7-113">키 유형은 ConnectionStrings, 키 및 ReadOnlyKeys의 값일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="6c3e7-114">기본값은 키입니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-114">Default is Keys.</span></span>

## <span data-ttu-id="6c3e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c3e7-115">PARAMETERS</span></span>

### <span data-ttu-id="6c3e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c3e7-116">-DefaultProfile</span></span>
<span data-ttu-id="6c3e7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c3e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c3e7-118">-InputObject</span></span>
<span data-ttu-id="6c3e7-119">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="6c3e7-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6c3e7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6c3e7-120">-Name</span></span>
<span data-ttu-id="6c3e7-121">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6c3e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c3e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c3e7-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-123">Name of resource group.</span></span>

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

### <span data-ttu-id="6c3e7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c3e7-124">-ResourceId</span></span>
<span data-ttu-id="6c3e7-125">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="6c3e7-126">-Type</span><span class="sxs-lookup"><span data-stu-id="6c3e7-126">-Type</span></span>
<span data-ttu-id="6c3e7-127">값: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="6c3e7-128">기본값은 키입니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-128">Default is Keys.</span></span>

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

### <span data-ttu-id="6c3e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3e7-129">CommonParameters</span></span>
<span data-ttu-id="6c3e7-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3e7-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c3e7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3e7-132">입력</span><span class="sxs-lookup"><span data-stu-id="6c3e7-132">INPUTS</span></span>

### <span data-ttu-id="6c3e7-133">없음</span><span class="sxs-lookup"><span data-stu-id="6c3e7-133">None</span></span>

## <span data-ttu-id="6c3e7-134">출력</span><span class="sxs-lookup"><span data-stu-id="6c3e7-134">OUTPUTS</span></span>

### <span data-ttu-id="6c3e7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="6c3e7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="6c3e7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="6c3e7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="6c3e7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="6c3e7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="6c3e7-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c3e7-138">NOTES</span></span>

## <span data-ttu-id="6c3e7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c3e7-139">RELATED LINKS</span></span>
