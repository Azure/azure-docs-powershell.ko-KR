---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201972"
---
# <span data-ttu-id="fdc74-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="fdc74-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="fdc74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdc74-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc74-103">대상 데이터베이스로 데이터베이스 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="fdc74-104">구문</span><span class="sxs-lookup"><span data-stu-id="fdc74-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fdc74-105">설명</span><span class="sxs-lookup"><span data-stu-id="fdc74-105">DESCRIPTION</span></span>
<span data-ttu-id="fdc74-106">대상 데이터베이스로 데이터베이스 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="fdc74-107">예제</span><span class="sxs-lookup"><span data-stu-id="fdc74-107">EXAMPLES</span></span>

### <span data-ttu-id="fdc74-108">예제 1: 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="fdc74-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="fdc74-109">이 명령은 데이터베이스 파일을 MyCache라는 Redis Enterprise Cache의 데이터베이스로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="fdc74-110">예제 2: 데이터베이스 가져오기(예제 파일 이름 사용)</span><span class="sxs-lookup"><span data-stu-id="fdc74-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="fdc74-111">이 명령은 데이터베이스 파일을 MyCache라는 Redis Enterprise Cache의 데이터베이스로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="fdc74-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdc74-112">PARAMETERS</span></span>

### <span data-ttu-id="fdc74-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdc74-113">-AsJob</span></span>
<span data-ttu-id="fdc74-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fdc74-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fdc74-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fdc74-115">-ClusterName</span></span>
<span data-ttu-id="fdc74-116">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="fdc74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc74-117">-DefaultProfile</span></span>
<span data-ttu-id="fdc74-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc74-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fdc74-119">-NoWait</span></span>
<span data-ttu-id="fdc74-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="fdc74-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fdc74-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdc74-121">-PassThru</span></span>
<span data-ttu-id="fdc74-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fdc74-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc74-123">-ResourceGroupName</span></span>
<span data-ttu-id="fdc74-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdc74-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="fdc74-125">-SasUri</span></span>
<span data-ttu-id="fdc74-126">가져올 대상 Blob에 대한 SAS Uri</span><span class="sxs-lookup"><span data-stu-id="fdc74-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="fdc74-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fdc74-127">-SubscriptionId</span></span>
<span data-ttu-id="fdc74-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fdc74-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fdc74-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdc74-130">-Confirm</span></span>
<span data-ttu-id="fdc74-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc74-132">-WhatIf</span></span>
<span data-ttu-id="fdc74-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fdc74-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdc74-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc74-135">CommonParameters</span></span>
<span data-ttu-id="fdc74-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc74-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fdc74-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc74-138">입력</span><span class="sxs-lookup"><span data-stu-id="fdc74-138">INPUTS</span></span>

## <span data-ttu-id="fdc74-139">출력</span><span class="sxs-lookup"><span data-stu-id="fdc74-139">OUTPUTS</span></span>

### <span data-ttu-id="fdc74-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fdc74-140">System.Boolean</span></span>

## <span data-ttu-id="fdc74-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fdc74-141">NOTES</span></span>

<span data-ttu-id="fdc74-142">별칭</span><span class="sxs-lookup"><span data-stu-id="fdc74-142">ALIASES</span></span>

## <span data-ttu-id="fdc74-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdc74-143">RELATED LINKS</span></span>

