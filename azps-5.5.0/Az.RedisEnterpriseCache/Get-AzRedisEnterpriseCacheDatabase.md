---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183780"
---
# <span data-ttu-id="c55bf-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="c55bf-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="c55bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c55bf-102">SYNOPSIS</span></span>
<span data-ttu-id="c55bf-103">RedisEnterprise 클러스터의 데이터베이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="c55bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="c55bf-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c55bf-105">설명</span><span class="sxs-lookup"><span data-stu-id="c55bf-105">DESCRIPTION</span></span>
<span data-ttu-id="c55bf-106">RedisEnterprise 클러스터의 데이터베이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="c55bf-107">예제</span><span class="sxs-lookup"><span data-stu-id="c55bf-107">EXAMPLES</span></span>

### <span data-ttu-id="c55bf-108">예제 1: 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="c55bf-109">이 명령은 MyCache라는 Redis Enterprise Cache에 대한 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="c55bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c55bf-110">PARAMETERS</span></span>

### <span data-ttu-id="c55bf-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c55bf-111">-ClusterName</span></span>
<span data-ttu-id="c55bf-112">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55bf-113">-DefaultProfile</span></span>
<span data-ttu-id="c55bf-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55bf-115">-ResourceGroupName</span></span>
<span data-ttu-id="c55bf-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55bf-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c55bf-117">-SubscriptionId</span></span>
<span data-ttu-id="c55bf-118">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c55bf-119">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55bf-120">CommonParameters</span></span>
<span data-ttu-id="c55bf-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c55bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55bf-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c55bf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55bf-123">입력</span><span class="sxs-lookup"><span data-stu-id="c55bf-123">INPUTS</span></span>

## <span data-ttu-id="c55bf-124">출력</span><span class="sxs-lookup"><span data-stu-id="c55bf-124">OUTPUTS</span></span>

### <span data-ttu-id="c55bf-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="c55bf-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="c55bf-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c55bf-126">NOTES</span></span>

<span data-ttu-id="c55bf-127">별칭</span><span class="sxs-lookup"><span data-stu-id="c55bf-127">ALIASES</span></span>

## <span data-ttu-id="c55bf-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c55bf-128">RELATED LINKS</span></span>

