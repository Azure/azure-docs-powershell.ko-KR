---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: e8554f0ac88cf3d69e36282b7e310cc92b41d6db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179084"
---
# <span data-ttu-id="2555e-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="2555e-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="2555e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2555e-102">SYNOPSIS</span></span>
<span data-ttu-id="2555e-103">기존 백업에서 PostgreSQL 유연한 서버 복원</span><span class="sxs-lookup"><span data-stu-id="2555e-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="2555e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2555e-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2555e-105">설명</span><span class="sxs-lookup"><span data-stu-id="2555e-105">DESCRIPTION</span></span>
<span data-ttu-id="2555e-106">기존 백업에서 서버 복원</span><span class="sxs-lookup"><span data-stu-id="2555e-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="2555e-107">예제</span><span class="sxs-lookup"><span data-stu-id="2555e-107">EXAMPLES</span></span>

### <span data-ttu-id="2555e-108">예제 1: PointInTime 복원을 사용하여 PostgreSql 서버 복원</span><span class="sxs-lookup"><span data-stu-id="2555e-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="2555e-109">이러한 cmdlet은 PointInTime 복원을 사용하여 PostgreSql 서버를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="2555e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2555e-110">PARAMETERS</span></span>

### <span data-ttu-id="2555e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2555e-111">-AsJob</span></span>
<span data-ttu-id="2555e-112">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="2555e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2555e-113">-DefaultProfile</span></span>
<span data-ttu-id="2555e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2555e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="2555e-115">-Location</span></span>
<span data-ttu-id="2555e-116">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2555e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2555e-117">-Name</span></span>
<span data-ttu-id="2555e-118">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2555e-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2555e-119">-NoWait</span></span>
<span data-ttu-id="2555e-120">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="2555e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2555e-121">-ResourceGroupName</span></span>
<span data-ttu-id="2555e-122">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2555e-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="2555e-123">-RestorePointInTime</span></span>
<span data-ttu-id="2555e-124">복원할 시점(ISO8601 형식)입니다(예: 2017-04-26T02:10:00+08:00).</span><span class="sxs-lookup"><span data-stu-id="2555e-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2555e-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="2555e-125">-SourceServerName</span></span>
<span data-ttu-id="2555e-126">원본 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-126">The name of the source server.</span></span>

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

### <span data-ttu-id="2555e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2555e-127">-SubscriptionId</span></span>
<span data-ttu-id="2555e-128">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2555e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2555e-129">-Confirm</span></span>
<span data-ttu-id="2555e-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2555e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2555e-131">-WhatIf</span></span>
<span data-ttu-id="2555e-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2555e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2555e-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2555e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2555e-134">CommonParameters</span></span>
<span data-ttu-id="2555e-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2555e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2555e-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2555e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2555e-137">입력</span><span class="sxs-lookup"><span data-stu-id="2555e-137">INPUTS</span></span>

## <span data-ttu-id="2555e-138">출력</span><span class="sxs-lookup"><span data-stu-id="2555e-138">OUTPUTS</span></span>

### <span data-ttu-id="2555e-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="2555e-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="2555e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2555e-140">NOTES</span></span>

<span data-ttu-id="2555e-141">별칭</span><span class="sxs-lookup"><span data-stu-id="2555e-141">ALIASES</span></span>

## <span data-ttu-id="2555e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2555e-142">RELATED LINKS</span></span>

