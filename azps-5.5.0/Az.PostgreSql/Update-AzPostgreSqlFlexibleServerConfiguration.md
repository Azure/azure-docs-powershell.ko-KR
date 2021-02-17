---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 82945caa08fb102c0ef5a05e95586f9c66d3d4a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183988"
---
# <span data-ttu-id="2c3af-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3af-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="2c3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c3af-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3af-103">서버의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="2c3af-104">AdministratorLoginPassword, Update-AzPostgreSqlFlexibleServer 업데이트하려는 경우 대신 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="2c3af-105">구문</span><span class="sxs-lookup"><span data-stu-id="2c3af-105">SYNTAX</span></span>

### <span data-ttu-id="2c3af-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="2c3af-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c3af-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2c3af-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c3af-108">설명</span><span class="sxs-lookup"><span data-stu-id="2c3af-108">DESCRIPTION</span></span>
<span data-ttu-id="2c3af-109">서버의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="2c3af-110">AdministratorLoginPassword, Update-AzPostgreSqlFlexibleServer 업데이트하려는 경우 대신 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="2c3af-111">예제</span><span class="sxs-lookup"><span data-stu-id="2c3af-111">EXAMPLES</span></span>

### <span data-ttu-id="2c3af-112">예제 1: 이름에 따라 Updatae가 지정된 PostgreSql 구성</span><span class="sxs-lookup"><span data-stu-id="2c3af-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="2c3af-113">이 cmdlet은 지정된 PostgreSql 구성을 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="2c3af-114">예제 1: ID에 따라 Updatae가 지정된 PostgreSql 구성</span><span class="sxs-lookup"><span data-stu-id="2c3af-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="2c3af-115">이 cmdlet은 ID에 따라 지정된 PostgreSql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="2c3af-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c3af-116">PARAMETERS</span></span>

### <span data-ttu-id="2c3af-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c3af-117">-AsJob</span></span>
<span data-ttu-id="2c3af-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2c3af-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2c3af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3af-119">-DefaultProfile</span></span>
<span data-ttu-id="2c3af-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c3af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c3af-121">-InputObject</span></span>
<span data-ttu-id="2c3af-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2c3af-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2c3af-123">-Name</span></span>
<span data-ttu-id="2c3af-124">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3af-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2c3af-125">-NoWait</span></span>
<span data-ttu-id="2c3af-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="2c3af-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2c3af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3af-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c3af-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-128">The name of the resource group.</span></span>
<span data-ttu-id="2c3af-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3af-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2c3af-130">-ServerName</span></span>
<span data-ttu-id="2c3af-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3af-132">-Source</span><span class="sxs-lookup"><span data-stu-id="2c3af-132">-Source</span></span>
<span data-ttu-id="2c3af-133">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="2c3af-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c3af-134">-SubscriptionId</span></span>
<span data-ttu-id="2c3af-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3af-136">-Value</span><span class="sxs-lookup"><span data-stu-id="2c3af-136">-Value</span></span>
<span data-ttu-id="2c3af-137">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="2c3af-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c3af-138">-Confirm</span></span>
<span data-ttu-id="2c3af-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3af-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3af-140">-WhatIf</span></span>
<span data-ttu-id="2c3af-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c3af-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3af-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3af-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3af-143">CommonParameters</span></span>
<span data-ttu-id="2c3af-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3af-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c3af-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3af-146">입력</span><span class="sxs-lookup"><span data-stu-id="2c3af-146">INPUTS</span></span>

### <span data-ttu-id="2c3af-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2c3af-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="2c3af-148">출력</span><span class="sxs-lookup"><span data-stu-id="2c3af-148">OUTPUTS</span></span>

### <span data-ttu-id="2c3af-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="2c3af-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="2c3af-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c3af-150">NOTES</span></span>

<span data-ttu-id="2c3af-151">별칭</span><span class="sxs-lookup"><span data-stu-id="2c3af-151">ALIASES</span></span>

<span data-ttu-id="2c3af-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2c3af-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c3af-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c3af-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c3af-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c3af-155">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2c3af-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c3af-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2c3af-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2c3af-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2c3af-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2c3af-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c3af-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2c3af-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2c3af-162">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="2c3af-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2c3af-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2c3af-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2c3af-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c3af-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2c3af-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c3af-167">RELATED LINKS</span></span>

