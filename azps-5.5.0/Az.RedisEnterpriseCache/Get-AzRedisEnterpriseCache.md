---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206104"
---
# <span data-ttu-id="5031b-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="5031b-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="5031b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5031b-102">SYNOPSIS</span></span>
<span data-ttu-id="5031b-103">RedisEnterprise 클러스터 및 관련 데이터베이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="5031b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5031b-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5031b-105">설명</span><span class="sxs-lookup"><span data-stu-id="5031b-105">DESCRIPTION</span></span>
<span data-ttu-id="5031b-106">RedisEnterprise 클러스터 및 관련 데이터베이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="5031b-107">예제</span><span class="sxs-lookup"><span data-stu-id="5031b-107">EXAMPLES</span></span>

### <span data-ttu-id="5031b-108">예제 1: 이름으로 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="5031b-109">이 명령은 MyCache라는 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="5031b-110">예제 2: 리소스 그룹의 모든 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="5031b-111">이 명령은 지정된 리소스 그룹에 있는 모든 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="5031b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5031b-112">PARAMETERS</span></span>

### <span data-ttu-id="5031b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5031b-113">-ClusterName</span></span>
<span data-ttu-id="5031b-114">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5031b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5031b-115">-DefaultProfile</span></span>
<span data-ttu-id="5031b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5031b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5031b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5031b-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5031b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5031b-119">-SubscriptionId</span></span>
<span data-ttu-id="5031b-120">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5031b-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5031b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5031b-122">CommonParameters</span></span>
<span data-ttu-id="5031b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5031b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5031b-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5031b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5031b-125">입력</span><span class="sxs-lookup"><span data-stu-id="5031b-125">INPUTS</span></span>

## <span data-ttu-id="5031b-126">출력</span><span class="sxs-lookup"><span data-stu-id="5031b-126">OUTPUTS</span></span>

### <span data-ttu-id="5031b-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="5031b-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="5031b-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5031b-128">NOTES</span></span>

<span data-ttu-id="5031b-129">별칭</span><span class="sxs-lookup"><span data-stu-id="5031b-129">ALIASES</span></span>

## <span data-ttu-id="5031b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5031b-130">RELATED LINKS</span></span>

