---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184017"
---
# <span data-ttu-id="1548f-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1548f-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="1548f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1548f-102">SYNOPSIS</span></span>
<span data-ttu-id="1548f-103">서버의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="1548f-104">AdministratorLoginPassword, Update-AzPostgreSqlServer 업데이트하려는 경우 대신 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="1548f-105">구문</span><span class="sxs-lookup"><span data-stu-id="1548f-105">SYNTAX</span></span>

### <span data-ttu-id="1548f-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="1548f-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1548f-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1548f-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1548f-108">설명</span><span class="sxs-lookup"><span data-stu-id="1548f-108">DESCRIPTION</span></span>
<span data-ttu-id="1548f-109">서버의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="1548f-110">AdministratorLoginPassword, Update-AzPostgreSqlServer 업데이트하려는 경우 대신 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="1548f-111">예제</span><span class="sxs-lookup"><span data-stu-id="1548f-111">EXAMPLES</span></span>

### <span data-ttu-id="1548f-112">예제 1: 이름으로 PostgreSql 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="1548f-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="1548f-113">이 cmdlet은 PostgreSql 구성을 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="1548f-114">예제 2: ID에 따라 PostgreSql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="1548f-115">이러한 cmdlet은 ID에 따라 PostgreSql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="1548f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1548f-116">PARAMETERS</span></span>

### <span data-ttu-id="1548f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1548f-117">-AsJob</span></span>
<span data-ttu-id="1548f-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1548f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1548f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1548f-119">-DefaultProfile</span></span>
<span data-ttu-id="1548f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1548f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1548f-121">-InputObject</span></span>
<span data-ttu-id="1548f-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1548f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1548f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1548f-123">-Name</span></span>
<span data-ttu-id="1548f-124">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="1548f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1548f-125">-NoWait</span></span>
<span data-ttu-id="1548f-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1548f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1548f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1548f-127">-ResourceGroupName</span></span>
<span data-ttu-id="1548f-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-128">The name of the resource group.</span></span>
<span data-ttu-id="1548f-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1548f-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1548f-130">-ServerName</span></span>
<span data-ttu-id="1548f-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-131">The name of the server.</span></span>

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

### <span data-ttu-id="1548f-132">-Source</span><span class="sxs-lookup"><span data-stu-id="1548f-132">-Source</span></span>
<span data-ttu-id="1548f-133">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="1548f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1548f-134">-SubscriptionId</span></span>
<span data-ttu-id="1548f-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1548f-136">-Value</span><span class="sxs-lookup"><span data-stu-id="1548f-136">-Value</span></span>
<span data-ttu-id="1548f-137">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="1548f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1548f-138">-Confirm</span></span>
<span data-ttu-id="1548f-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1548f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1548f-140">-WhatIf</span></span>
<span data-ttu-id="1548f-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1548f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1548f-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1548f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1548f-143">CommonParameters</span></span>
<span data-ttu-id="1548f-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1548f-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1548f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1548f-146">입력</span><span class="sxs-lookup"><span data-stu-id="1548f-146">INPUTS</span></span>

### <span data-ttu-id="1548f-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1548f-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1548f-148">출력</span><span class="sxs-lookup"><span data-stu-id="1548f-148">OUTPUTS</span></span>

### <span data-ttu-id="1548f-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="1548f-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="1548f-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1548f-150">NOTES</span></span>

<span data-ttu-id="1548f-151">별칭</span><span class="sxs-lookup"><span data-stu-id="1548f-151">ALIASES</span></span>

<span data-ttu-id="1548f-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1548f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1548f-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1548f-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1548f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1548f-155">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1548f-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1548f-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1548f-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1548f-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1548f-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1548f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1548f-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1548f-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1548f-162">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="1548f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1548f-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1548f-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1548f-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1548f-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1548f-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1548f-167">RELATED LINKS</span></span>

