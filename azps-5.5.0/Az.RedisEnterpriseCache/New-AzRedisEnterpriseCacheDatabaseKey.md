---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201961"
---
# <span data-ttu-id="c0815-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="c0815-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="c0815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0815-102">SYNOPSIS</span></span>
<span data-ttu-id="c0815-103">RedisEnterprise 데이터베이스의 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="c0815-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0815-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0815-105">설명</span><span class="sxs-lookup"><span data-stu-id="c0815-105">DESCRIPTION</span></span>
<span data-ttu-id="c0815-106">RedisEnterprise 데이터베이스의 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="c0815-107">예제</span><span class="sxs-lookup"><span data-stu-id="c0815-107">EXAMPLES</span></span>

### <span data-ttu-id="c0815-108">예제 1: 기본 액세스 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="c0815-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="c0815-109">이 명령은 MyCache라는 Redis Enterprise Cache의 데이터베이스에 대한 연결을 인증하는 데 사용되는 기본 비밀 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="c0815-110">예제 2: 보조 액세스 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="c0815-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="c0815-111">이 명령은 MyCache라는 Redis Enterprise Cache의 데이터베이스에 대한 연결을 인증하는 데 사용되는 보조 비밀 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="c0815-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0815-112">PARAMETERS</span></span>

### <span data-ttu-id="c0815-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0815-113">-AsJob</span></span>
<span data-ttu-id="c0815-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c0815-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0815-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0815-115">-ClusterName</span></span>
<span data-ttu-id="c0815-116">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="c0815-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0815-117">-DefaultProfile</span></span>
<span data-ttu-id="c0815-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0815-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c0815-119">-KeyType</span></span>
<span data-ttu-id="c0815-120">다시 생성하기 위한 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0815-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0815-121">-NoWait</span></span>
<span data-ttu-id="c0815-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="c0815-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0815-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0815-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0815-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0815-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0815-125">-SubscriptionId</span></span>
<span data-ttu-id="c0815-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0815-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0815-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0815-128">-Confirm</span></span>
<span data-ttu-id="c0815-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0815-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0815-130">-WhatIf</span></span>
<span data-ttu-id="c0815-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c0815-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0815-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0815-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0815-133">CommonParameters</span></span>
<span data-ttu-id="c0815-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0815-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0815-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0815-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0815-136">입력</span><span class="sxs-lookup"><span data-stu-id="c0815-136">INPUTS</span></span>

## <span data-ttu-id="c0815-137">출력</span><span class="sxs-lookup"><span data-stu-id="c0815-137">OUTPUTS</span></span>

### <span data-ttu-id="c0815-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c0815-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="c0815-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0815-139">NOTES</span></span>

<span data-ttu-id="c0815-140">별칭</span><span class="sxs-lookup"><span data-stu-id="c0815-140">ALIASES</span></span>

## <span data-ttu-id="c0815-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0815-141">RELATED LINKS</span></span>

