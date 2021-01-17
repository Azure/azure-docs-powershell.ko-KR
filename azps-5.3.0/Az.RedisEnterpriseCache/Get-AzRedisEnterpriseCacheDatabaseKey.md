---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490675"
---
# <span data-ttu-id="d72d1-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="d72d1-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="d72d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d72d1-103">RedisEnterprise 데이터베이스에 대한 액세스 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="d72d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d72d1-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d72d1-105">설명</span><span class="sxs-lookup"><span data-stu-id="d72d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d72d1-106">RedisEnterprise 데이터베이스에 대한 액세스 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="d72d1-107">예제</span><span class="sxs-lookup"><span data-stu-id="d72d1-107">EXAMPLES</span></span>

### <span data-ttu-id="d72d1-108">예제 1: 데이터베이스 액세스 키 얻기</span><span class="sxs-lookup"><span data-stu-id="d72d1-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="d72d1-109">이 명령은 MyCache라는 Redis Enterprise Cache의 데이터베이스에 대한 연결을 인증하는 데 사용되는 비밀 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="d72d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d72d1-110">PARAMETERS</span></span>

### <span data-ttu-id="d72d1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d72d1-111">-ClusterName</span></span>
<span data-ttu-id="d72d1-112">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="d72d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72d1-113">-DefaultProfile</span></span>
<span data-ttu-id="d72d1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d72d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="d72d1-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="d72d1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d72d1-117">-SubscriptionId</span></span>
<span data-ttu-id="d72d1-118">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d72d1-119">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d72d1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d72d1-120">-Confirm</span></span>
<span data-ttu-id="d72d1-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72d1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72d1-122">-WhatIf</span></span>
<span data-ttu-id="d72d1-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d72d1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72d1-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72d1-125">CommonParameters</span></span>
<span data-ttu-id="d72d1-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d72d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72d1-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d72d1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72d1-128">입력</span><span class="sxs-lookup"><span data-stu-id="d72d1-128">INPUTS</span></span>

## <span data-ttu-id="d72d1-129">출력</span><span class="sxs-lookup"><span data-stu-id="d72d1-129">OUTPUTS</span></span>

### <span data-ttu-id="d72d1-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d72d1-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="d72d1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d72d1-131">NOTES</span></span>

<span data-ttu-id="d72d1-132">별칭</span><span class="sxs-lookup"><span data-stu-id="d72d1-132">ALIASES</span></span>

## <span data-ttu-id="d72d1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d72d1-133">RELATED LINKS</span></span>

