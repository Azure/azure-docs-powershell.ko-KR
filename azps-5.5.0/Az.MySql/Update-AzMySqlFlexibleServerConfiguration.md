---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190028"
---
# <span data-ttu-id="b1022-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1022-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="b1022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1022-102">SYNOPSIS</span></span>
<span data-ttu-id="b1022-103">MySQL 유연한 서버의 구성에 대한 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="b1022-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1022-104">SYNTAX</span></span>

### <span data-ttu-id="b1022-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1022-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1022-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b1022-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1022-107">설명</span><span class="sxs-lookup"><span data-stu-id="b1022-107">DESCRIPTION</span></span>
<span data-ttu-id="b1022-108">MySQL 유연한 서버의 구성에 대한 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="b1022-109">예제</span><span class="sxs-lookup"><span data-stu-id="b1022-109">EXAMPLES</span></span>

### <span data-ttu-id="b1022-110">예제 1: 이름으로 MySql 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="b1022-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="b1022-111">이 cmdlet은 이름으로 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="b1022-112">예제 2: ID로 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="b1022-113">이러한 cmdlet은 ID에 따라 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="b1022-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1022-114">PARAMETERS</span></span>

### <span data-ttu-id="b1022-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1022-115">-AsJob</span></span>
<span data-ttu-id="b1022-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b1022-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b1022-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1022-117">-DefaultProfile</span></span>
<span data-ttu-id="b1022-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1022-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1022-119">-InputObject</span></span>
<span data-ttu-id="b1022-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b1022-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1022-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1022-121">-Name</span></span>
<span data-ttu-id="b1022-122">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="b1022-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1022-123">-NoWait</span></span>
<span data-ttu-id="b1022-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="b1022-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b1022-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1022-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1022-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-126">The name of the resource group.</span></span>
<span data-ttu-id="b1022-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b1022-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1022-128">-ServerName</span></span>
<span data-ttu-id="b1022-129">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-129">The name of the server.</span></span>

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

### <span data-ttu-id="b1022-130">-Source</span><span class="sxs-lookup"><span data-stu-id="b1022-130">-Source</span></span>
<span data-ttu-id="b1022-131">업데이트 값의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-131">The source of the updating value.</span></span>
<span data-ttu-id="b1022-132">기본값은 user-override입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-132">The default value is user-override</span></span>

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

### <span data-ttu-id="b1022-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1022-133">-SubscriptionId</span></span>
<span data-ttu-id="b1022-134">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b1022-135">-Value</span><span class="sxs-lookup"><span data-stu-id="b1022-135">-Value</span></span>
<span data-ttu-id="b1022-136">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="b1022-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1022-137">-Confirm</span></span>
<span data-ttu-id="b1022-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1022-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1022-139">-WhatIf</span></span>
<span data-ttu-id="b1022-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1022-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1022-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1022-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1022-142">CommonParameters</span></span>
<span data-ttu-id="b1022-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1022-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1022-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1022-145">입력</span><span class="sxs-lookup"><span data-stu-id="b1022-145">INPUTS</span></span>

### <span data-ttu-id="b1022-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b1022-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b1022-147">출력</span><span class="sxs-lookup"><span data-stu-id="b1022-147">OUTPUTS</span></span>

### <span data-ttu-id="b1022-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b1022-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="b1022-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1022-149">NOTES</span></span>

<span data-ttu-id="b1022-150">별칭</span><span class="sxs-lookup"><span data-stu-id="b1022-150">ALIASES</span></span>

<span data-ttu-id="b1022-151">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b1022-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1022-152">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1022-153">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1022-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1022-154">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b1022-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1022-155">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b1022-156">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b1022-157">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b1022-158">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b1022-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1022-159">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b1022-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b1022-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b1022-162">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="b1022-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b1022-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b1022-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b1022-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1022-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b1022-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1022-167">RELATED LINKS</span></span>

