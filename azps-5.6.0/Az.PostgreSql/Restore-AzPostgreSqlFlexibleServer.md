---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953600"
---
# <span data-ttu-id="38759-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="38759-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="38759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38759-102">SYNOPSIS</span></span>
<span data-ttu-id="38759-103">기존 백업에서 PostgreSQL 유연한 서버 복원</span><span class="sxs-lookup"><span data-stu-id="38759-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="38759-104">구문</span><span class="sxs-lookup"><span data-stu-id="38759-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38759-105">설명</span><span class="sxs-lookup"><span data-stu-id="38759-105">DESCRIPTION</span></span>
<span data-ttu-id="38759-106">기존 백업에서 서버 복원</span><span class="sxs-lookup"><span data-stu-id="38759-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="38759-107">예제</span><span class="sxs-lookup"><span data-stu-id="38759-107">EXAMPLES</span></span>

### <span data-ttu-id="38759-108">예제 1: PointInTime 복원을 사용하여 PostgreSql 서버 복원</span><span class="sxs-lookup"><span data-stu-id="38759-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="38759-109">이러한 cmdlet은 PointInTime 복원을 사용하여 PostgreSql 서버를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="38759-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="38759-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="38759-110">PARAMETERS</span></span>

### <span data-ttu-id="38759-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38759-111">-AsJob</span></span>
<span data-ttu-id="38759-112">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38759-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="38759-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38759-113">-DefaultProfile</span></span>
<span data-ttu-id="38759-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38759-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38759-115">-Location</span><span class="sxs-lookup"><span data-stu-id="38759-115">-Location</span></span>
<span data-ttu-id="38759-116">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="38759-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="38759-117">-Name</span><span class="sxs-lookup"><span data-stu-id="38759-117">-Name</span></span>
<span data-ttu-id="38759-118">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38759-118">The name of the server.</span></span>

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

### <span data-ttu-id="38759-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="38759-119">-NoWait</span></span>
<span data-ttu-id="38759-120">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38759-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="38759-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38759-121">-ResourceGroupName</span></span>
<span data-ttu-id="38759-122">리소스를 포함하는 리소스 그룹의 이름, Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38759-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="38759-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="38759-123">-RestorePointInTime</span></span>
<span data-ttu-id="38759-124">복원할 시점(ISO8601 형식) (예: 2017-04-26T02:10:00+08:00).</span><span class="sxs-lookup"><span data-stu-id="38759-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

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

### <span data-ttu-id="38759-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="38759-125">-SourceServerName</span></span>
<span data-ttu-id="38759-126">원본 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38759-126">The name of the source server.</span></span>

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

### <span data-ttu-id="38759-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38759-127">-SubscriptionId</span></span>
<span data-ttu-id="38759-128">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="38759-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="38759-129">-Zone</span><span class="sxs-lookup"><span data-stu-id="38759-129">-Zone</span></span>
<span data-ttu-id="38759-130">리소스를 프로비전할 가용성 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="38759-130">Availability zone into which to provision the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38759-131">-확인</span><span class="sxs-lookup"><span data-stu-id="38759-131">-Confirm</span></span>
<span data-ttu-id="38759-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38759-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38759-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38759-133">-WhatIf</span></span>
<span data-ttu-id="38759-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="38759-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38759-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38759-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38759-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38759-136">CommonParameters</span></span>
<span data-ttu-id="38759-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38759-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38759-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38759-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38759-139">입력</span><span class="sxs-lookup"><span data-stu-id="38759-139">INPUTS</span></span>

## <span data-ttu-id="38759-140">출력</span><span class="sxs-lookup"><span data-stu-id="38759-140">OUTPUTS</span></span>

### <span data-ttu-id="38759-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="38759-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="38759-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38759-142">NOTES</span></span>

<span data-ttu-id="38759-143">별칭</span><span class="sxs-lookup"><span data-stu-id="38759-143">ALIASES</span></span>

## <span data-ttu-id="38759-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38759-144">RELATED LINKS</span></span>

