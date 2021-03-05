---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: fd127005107586e31798d215d7f54888b26705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000832"
---
# <span data-ttu-id="259ec-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="259ec-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="259ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="259ec-102">SYNOPSIS</span></span>
<span data-ttu-id="259ec-103">RedisEnterprise 클러스터 및 해당 관련 데이터베이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="259ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="259ec-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="259ec-105">설명</span><span class="sxs-lookup"><span data-stu-id="259ec-105">DESCRIPTION</span></span>
<span data-ttu-id="259ec-106">RedisEnterprise 클러스터 및 해당 관련 데이터베이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="259ec-107">예제</span><span class="sxs-lookup"><span data-stu-id="259ec-107">EXAMPLES</span></span>

### <span data-ttu-id="259ec-108">예제 1: 이름에 의해 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="259ec-109">이 명령은 MyCache라는 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="259ec-110">예제 2: 리소스 그룹의 모든 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="259ec-111">이 명령은 지정된 리소스 그룹의 모든 Redis Enterprise Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="259ec-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="259ec-112">PARAMETERS</span></span>

### <span data-ttu-id="259ec-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="259ec-113">-ClusterName</span></span>
<span data-ttu-id="259ec-114">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="259ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259ec-115">-DefaultProfile</span></span>
<span data-ttu-id="259ec-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="259ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="259ec-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="259ec-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="259ec-119">-SubscriptionId</span></span>
<span data-ttu-id="259ec-120">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="259ec-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="259ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259ec-122">CommonParameters</span></span>
<span data-ttu-id="259ec-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="259ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259ec-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="259ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259ec-125">입력</span><span class="sxs-lookup"><span data-stu-id="259ec-125">INPUTS</span></span>

## <span data-ttu-id="259ec-126">출력</span><span class="sxs-lookup"><span data-stu-id="259ec-126">OUTPUTS</span></span>

### <span data-ttu-id="259ec-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="259ec-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="259ec-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="259ec-128">NOTES</span></span>

<span data-ttu-id="259ec-129">별칭</span><span class="sxs-lookup"><span data-stu-id="259ec-129">ALIASES</span></span>

## <span data-ttu-id="259ec-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="259ec-130">RELATED LINKS</span></span>

