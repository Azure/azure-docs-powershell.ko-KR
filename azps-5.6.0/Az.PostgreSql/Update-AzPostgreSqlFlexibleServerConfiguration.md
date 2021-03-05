---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: e45d342f7bb02034b2adf0473e6d4d1eb3c2b370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974656"
---
# <span data-ttu-id="3ee39-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ee39-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="3ee39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee39-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee39-103">서버 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="3ee39-104">AdministratorLoginPassword, sku 등을 업데이트하려는 경우 대신 Update-AzPostgreSqlFlexibleServer 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="3ee39-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="3ee39-105">구문</span><span class="sxs-lookup"><span data-stu-id="3ee39-105">SYNTAX</span></span>

### <span data-ttu-id="3ee39-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="3ee39-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ee39-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3ee39-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ee39-108">설명</span><span class="sxs-lookup"><span data-stu-id="3ee39-108">DESCRIPTION</span></span>
<span data-ttu-id="3ee39-109">서버 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="3ee39-110">AdministratorLoginPassword, sku 등을 업데이트하려는 경우 대신 Update-AzPostgreSqlFlexibleServer 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="3ee39-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="3ee39-111">예제</span><span class="sxs-lookup"><span data-stu-id="3ee39-111">EXAMPLES</span></span>

### <span data-ttu-id="3ee39-112">예제 1: Updatae 지정 PostgreSql 구성 이름</span><span class="sxs-lookup"><span data-stu-id="3ee39-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="3ee39-113">이 cmdlet은 이름을 통해 PostgreSql 구성을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="3ee39-114">예제 1: ID에 따라 Updatae 지정 PostgreSql 구성</span><span class="sxs-lookup"><span data-stu-id="3ee39-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="3ee39-115">이 cmdlet은 ID에 따라 PostgreSql 구성을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="3ee39-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ee39-116">PARAMETERS</span></span>

### <span data-ttu-id="3ee39-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ee39-117">-AsJob</span></span>
<span data-ttu-id="3ee39-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3ee39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee39-119">-DefaultProfile</span></span>
<span data-ttu-id="3ee39-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee39-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ee39-121">-InputObject</span></span>
<span data-ttu-id="3ee39-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3ee39-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ee39-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3ee39-123">-Name</span></span>
<span data-ttu-id="3ee39-124">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="3ee39-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ee39-125">-NoWait</span></span>
<span data-ttu-id="3ee39-126">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="3ee39-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ee39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee39-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ee39-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-128">The name of the resource group.</span></span>
<span data-ttu-id="3ee39-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3ee39-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ee39-130">-ServerName</span></span>
<span data-ttu-id="3ee39-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-131">The name of the server.</span></span>

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

### <span data-ttu-id="3ee39-132">-Source</span><span class="sxs-lookup"><span data-stu-id="3ee39-132">-Source</span></span>
<span data-ttu-id="3ee39-133">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="3ee39-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ee39-134">-SubscriptionId</span></span>
<span data-ttu-id="3ee39-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3ee39-136">-Value</span><span class="sxs-lookup"><span data-stu-id="3ee39-136">-Value</span></span>
<span data-ttu-id="3ee39-137">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="3ee39-138">-확인</span><span class="sxs-lookup"><span data-stu-id="3ee39-138">-Confirm</span></span>
<span data-ttu-id="3ee39-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ee39-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee39-140">-WhatIf</span></span>
<span data-ttu-id="3ee39-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ee39-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ee39-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee39-143">CommonParameters</span></span>
<span data-ttu-id="3ee39-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee39-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ee39-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee39-146">입력</span><span class="sxs-lookup"><span data-stu-id="3ee39-146">INPUTS</span></span>

### <span data-ttu-id="3ee39-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3ee39-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3ee39-148">출력</span><span class="sxs-lookup"><span data-stu-id="3ee39-148">OUTPUTS</span></span>

### <span data-ttu-id="3ee39-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="3ee39-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="3ee39-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ee39-150">NOTES</span></span>

<span data-ttu-id="3ee39-151">별칭</span><span class="sxs-lookup"><span data-stu-id="3ee39-151">ALIASES</span></span>

<span data-ttu-id="3ee39-152">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3ee39-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ee39-153">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ee39-154">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ee39-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ee39-155">INPUTOBJECT <IPostgreSqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ee39-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ee39-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3ee39-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3ee39-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3ee39-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3ee39-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ee39-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3ee39-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3ee39-162">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="3ee39-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3ee39-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3ee39-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3ee39-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee39-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3ee39-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ee39-167">RELATED LINKS</span></span>

