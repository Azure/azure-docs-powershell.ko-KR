---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183785"
---
# <span data-ttu-id="88176-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="88176-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="88176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88176-102">SYNOPSIS</span></span>
<span data-ttu-id="88176-103">대상 데이터베이스에서 데이터베이스 파일을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88176-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="88176-104">구문</span><span class="sxs-lookup"><span data-stu-id="88176-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="88176-105">설명</span><span class="sxs-lookup"><span data-stu-id="88176-105">DESCRIPTION</span></span>
<span data-ttu-id="88176-106">대상 데이터베이스에서 데이터베이스 파일을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88176-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="88176-107">예제</span><span class="sxs-lookup"><span data-stu-id="88176-107">EXAMPLES</span></span>

### <span data-ttu-id="88176-108">예제 1: 데이터베이스 내보내기</span><span class="sxs-lookup"><span data-stu-id="88176-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="88176-109">이 명령은 MyCache라는 Redis Enterprise Cache의 데이터베이스를 데이터베이스 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88176-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="88176-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88176-110">PARAMETERS</span></span>

### <span data-ttu-id="88176-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88176-111">-AsJob</span></span>
<span data-ttu-id="88176-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="88176-112">Run the command as a job</span></span>

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

### <span data-ttu-id="88176-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="88176-113">-ClusterName</span></span>
<span data-ttu-id="88176-114">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88176-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="88176-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88176-115">-DefaultProfile</span></span>
<span data-ttu-id="88176-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88176-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88176-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="88176-117">-NoWait</span></span>
<span data-ttu-id="88176-118">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="88176-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88176-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88176-119">-PassThru</span></span>
<span data-ttu-id="88176-120">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="88176-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="88176-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88176-121">-ResourceGroupName</span></span>
<span data-ttu-id="88176-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88176-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="88176-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="88176-123">-SasUri</span></span>
<span data-ttu-id="88176-124">내보낼 대상 디렉터리에 대한 SAS Uri</span><span class="sxs-lookup"><span data-stu-id="88176-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="88176-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88176-125">-SubscriptionId</span></span>
<span data-ttu-id="88176-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88176-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="88176-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="88176-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88176-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88176-128">-Confirm</span></span>
<span data-ttu-id="88176-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88176-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88176-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88176-130">-WhatIf</span></span>
<span data-ttu-id="88176-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="88176-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88176-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88176-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88176-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88176-133">CommonParameters</span></span>
<span data-ttu-id="88176-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88176-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88176-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88176-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88176-136">입력</span><span class="sxs-lookup"><span data-stu-id="88176-136">INPUTS</span></span>

## <span data-ttu-id="88176-137">출력</span><span class="sxs-lookup"><span data-stu-id="88176-137">OUTPUTS</span></span>

### <span data-ttu-id="88176-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88176-138">System.Boolean</span></span>

## <span data-ttu-id="88176-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88176-139">NOTES</span></span>

<span data-ttu-id="88176-140">별칭</span><span class="sxs-lookup"><span data-stu-id="88176-140">ALIASES</span></span>

## <span data-ttu-id="88176-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88176-141">RELATED LINKS</span></span>

