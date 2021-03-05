---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ff635c55600c6528ecad537b74a843e2d1da830e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000795"
---
# <span data-ttu-id="65d63-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="65d63-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="65d63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d63-102">SYNOPSIS</span></span>
<span data-ttu-id="65d63-103">RedisEnterprise 데이터베이스에 대한 액세스 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="65d63-104">구문</span><span class="sxs-lookup"><span data-stu-id="65d63-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65d63-105">설명</span><span class="sxs-lookup"><span data-stu-id="65d63-105">DESCRIPTION</span></span>
<span data-ttu-id="65d63-106">RedisEnterprise 데이터베이스에 대한 액세스 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="65d63-107">예제</span><span class="sxs-lookup"><span data-stu-id="65d63-107">EXAMPLES</span></span>

### <span data-ttu-id="65d63-108">예제 1: 데이터베이스 액세스 키 사용</span><span class="sxs-lookup"><span data-stu-id="65d63-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="65d63-109">이 명령은 MyCache라는 Redis Enterprise Cache의 데이터베이스에 대한 연결을 인증하는 데 사용되는 비밀 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="65d63-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65d63-110">PARAMETERS</span></span>

### <span data-ttu-id="65d63-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="65d63-111">-ClusterName</span></span>
<span data-ttu-id="65d63-112">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="65d63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d63-113">-DefaultProfile</span></span>
<span data-ttu-id="65d63-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d63-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d63-115">-ResourceGroupName</span></span>
<span data-ttu-id="65d63-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="65d63-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65d63-117">-SubscriptionId</span></span>
<span data-ttu-id="65d63-118">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="65d63-119">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="65d63-120">-확인</span><span class="sxs-lookup"><span data-stu-id="65d63-120">-Confirm</span></span>
<span data-ttu-id="65d63-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d63-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d63-122">-WhatIf</span></span>
<span data-ttu-id="65d63-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d63-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d63-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d63-125">CommonParameters</span></span>
<span data-ttu-id="65d63-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65d63-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d63-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65d63-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d63-128">입력</span><span class="sxs-lookup"><span data-stu-id="65d63-128">INPUTS</span></span>

## <span data-ttu-id="65d63-129">출력</span><span class="sxs-lookup"><span data-stu-id="65d63-129">OUTPUTS</span></span>

### <span data-ttu-id="65d63-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="65d63-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="65d63-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65d63-131">NOTES</span></span>

<span data-ttu-id="65d63-132">별칭</span><span class="sxs-lookup"><span data-stu-id="65d63-132">ALIASES</span></span>

## <span data-ttu-id="65d63-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65d63-133">RELATED LINKS</span></span>

