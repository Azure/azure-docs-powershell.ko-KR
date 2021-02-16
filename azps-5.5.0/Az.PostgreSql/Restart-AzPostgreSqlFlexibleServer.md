---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 9c1a0d2746b40402982f1e904548d92f2776819f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179097"
---
# <span data-ttu-id="fad9f-101">Restart-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="fad9f-101">Restart-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="fad9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fad9f-102">SYNOPSIS</span></span>
<span data-ttu-id="fad9f-103">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-103">Restarts a server.</span></span>

## <span data-ttu-id="fad9f-104">구문</span><span class="sxs-lookup"><span data-stu-id="fad9f-104">SYNTAX</span></span>

### <span data-ttu-id="fad9f-105">다시 시작(기본값)</span><span class="sxs-lookup"><span data-stu-id="fad9f-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fad9f-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fad9f-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fad9f-107">설명</span><span class="sxs-lookup"><span data-stu-id="fad9f-107">DESCRIPTION</span></span>
<span data-ttu-id="fad9f-108">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-108">Restarts a server.</span></span>

## <span data-ttu-id="fad9f-109">예제</span><span class="sxs-lookup"><span data-stu-id="fad9f-109">EXAMPLES</span></span>

### <span data-ttu-id="fad9f-110">예제 1: 리소스 이름으로 서버 다시 시작</span><span class="sxs-lookup"><span data-stu-id="fad9f-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="fad9f-111">이름으로 서버 다시 시작</span><span class="sxs-lookup"><span data-stu-id="fad9f-111">Restart the server by name</span></span>

### <span data-ttu-id="fad9f-112">예제 2: ID로 서버 다시 시작</span><span class="sxs-lookup"><span data-stu-id="fad9f-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/restart"
PS C:\> Restart-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="fad9f-113">ID로 서버 다시 시작</span><span class="sxs-lookup"><span data-stu-id="fad9f-113">Restart the server by identity</span></span>

## <span data-ttu-id="fad9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fad9f-114">PARAMETERS</span></span>

### <span data-ttu-id="fad9f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fad9f-115">-AsJob</span></span>
<span data-ttu-id="fad9f-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fad9f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fad9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad9f-117">-DefaultProfile</span></span>
<span data-ttu-id="fad9f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fad9f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fad9f-119">-InputObject</span></span>
<span data-ttu-id="fad9f-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="fad9f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fad9f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fad9f-121">-Name</span></span>
<span data-ttu-id="fad9f-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad9f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fad9f-123">-NoWait</span></span>
<span data-ttu-id="fad9f-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="fad9f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fad9f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fad9f-125">-PassThru</span></span>
<span data-ttu-id="fad9f-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fad9f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad9f-127">-ResourceGroupName</span></span>
<span data-ttu-id="fad9f-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-128">The name of the resource group.</span></span>
<span data-ttu-id="fad9f-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad9f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fad9f-130">-SubscriptionId</span></span>
<span data-ttu-id="fad9f-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad9f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fad9f-132">-Confirm</span></span>
<span data-ttu-id="fad9f-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fad9f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fad9f-134">-WhatIf</span></span>
<span data-ttu-id="fad9f-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fad9f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fad9f-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fad9f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad9f-137">CommonParameters</span></span>
<span data-ttu-id="fad9f-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad9f-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fad9f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad9f-140">입력</span><span class="sxs-lookup"><span data-stu-id="fad9f-140">INPUTS</span></span>

### <span data-ttu-id="fad9f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fad9f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fad9f-142">출력</span><span class="sxs-lookup"><span data-stu-id="fad9f-142">OUTPUTS</span></span>

### <span data-ttu-id="fad9f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fad9f-143">System.Boolean</span></span>

## <span data-ttu-id="fad9f-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fad9f-144">NOTES</span></span>

<span data-ttu-id="fad9f-145">별칭</span><span class="sxs-lookup"><span data-stu-id="fad9f-145">ALIASES</span></span>

<span data-ttu-id="fad9f-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="fad9f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fad9f-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fad9f-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fad9f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fad9f-149">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fad9f-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fad9f-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fad9f-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fad9f-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fad9f-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="fad9f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fad9f-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fad9f-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fad9f-156">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="fad9f-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fad9f-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fad9f-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fad9f-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fad9f-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fad9f-161">RELATED LINKS</span></span>

