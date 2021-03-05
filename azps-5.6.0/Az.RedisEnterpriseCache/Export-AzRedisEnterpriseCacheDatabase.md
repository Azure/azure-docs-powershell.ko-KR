---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000843"
---
# <span data-ttu-id="a0e8e-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="a0e8e-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="a0e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e8e-103">대상 데이터베이스에서 데이터베이스 파일을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="a0e8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0e8e-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e8e-105">설명</span><span class="sxs-lookup"><span data-stu-id="a0e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e8e-106">대상 데이터베이스에서 데이터베이스 파일을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="a0e8e-107">예제</span><span class="sxs-lookup"><span data-stu-id="a0e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e8e-108">예제 1: 데이터베이스 내보내기</span><span class="sxs-lookup"><span data-stu-id="a0e8e-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="a0e8e-109">이 명령은 MyCache라는 Redis Enterprise Cache의 데이터베이스를 데이터베이스 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="a0e8e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a0e8e-110">PARAMETERS</span></span>

### <span data-ttu-id="a0e8e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0e8e-111">-AsJob</span></span>
<span data-ttu-id="a0e8e-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a0e8e-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a0e8e-113">-ClusterName</span></span>
<span data-ttu-id="a0e8e-114">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="a0e8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e8e-115">-DefaultProfile</span></span>
<span data-ttu-id="a0e8e-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0e8e-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a0e8e-117">-NoWait</span></span>
<span data-ttu-id="a0e8e-118">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="a0e8e-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0e8e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0e8e-119">-PassThru</span></span>
<span data-ttu-id="a0e8e-120">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a0e8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0e8e-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0e8e-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="a0e8e-123">-SasUri</span></span>
<span data-ttu-id="a0e8e-124">내보낼 대상 디렉터리에 대한 SAS Uri</span><span class="sxs-lookup"><span data-stu-id="a0e8e-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="a0e8e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0e8e-125">-SubscriptionId</span></span>
<span data-ttu-id="a0e8e-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0e8e-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0e8e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a0e8e-128">-Confirm</span></span>
<span data-ttu-id="a0e8e-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e8e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e8e-130">-WhatIf</span></span>
<span data-ttu-id="a0e8e-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e8e-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e8e-133">CommonParameters</span></span>
<span data-ttu-id="a0e8e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0e8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e8e-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0e8e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e8e-136">입력</span><span class="sxs-lookup"><span data-stu-id="a0e8e-136">INPUTS</span></span>

## <span data-ttu-id="a0e8e-137">출력</span><span class="sxs-lookup"><span data-stu-id="a0e8e-137">OUTPUTS</span></span>

### <span data-ttu-id="a0e8e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0e8e-138">System.Boolean</span></span>

## <span data-ttu-id="a0e8e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0e8e-139">NOTES</span></span>

<span data-ttu-id="a0e8e-140">별칭</span><span class="sxs-lookup"><span data-stu-id="a0e8e-140">ALIASES</span></span>

## <span data-ttu-id="a0e8e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0e8e-141">RELATED LINKS</span></span>

