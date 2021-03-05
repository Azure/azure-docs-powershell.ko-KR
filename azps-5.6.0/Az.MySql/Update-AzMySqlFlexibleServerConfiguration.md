---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968784"
---
# <span data-ttu-id="755cb-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="755cb-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="755cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755cb-102">SYNOPSIS</span></span>
<span data-ttu-id="755cb-103">MySQL 유연한 서버 구성에 대한 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="755cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="755cb-104">SYNTAX</span></span>

### <span data-ttu-id="755cb-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="755cb-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="755cb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="755cb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="755cb-107">설명</span><span class="sxs-lookup"><span data-stu-id="755cb-107">DESCRIPTION</span></span>
<span data-ttu-id="755cb-108">MySQL 유연한 서버 구성에 대한 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="755cb-109">예제</span><span class="sxs-lookup"><span data-stu-id="755cb-109">EXAMPLES</span></span>

### <span data-ttu-id="755cb-110">예제 1: 이름에 따라 MySql 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="755cb-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="755cb-111">이 cmdlet은 이름으로 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="755cb-112">예제 2: ID에 따라 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="755cb-113">이러한 cmdlet은 ID에 따라 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="755cb-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="755cb-114">PARAMETERS</span></span>

### <span data-ttu-id="755cb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="755cb-115">-AsJob</span></span>
<span data-ttu-id="755cb-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="755cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755cb-117">-DefaultProfile</span></span>
<span data-ttu-id="755cb-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="755cb-119">-InputObject</span></span>
<span data-ttu-id="755cb-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="755cb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="755cb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="755cb-121">-Name</span></span>
<span data-ttu-id="755cb-122">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="755cb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="755cb-123">-NoWait</span></span>
<span data-ttu-id="755cb-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="755cb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="755cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="755cb-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-126">The name of the resource group.</span></span>
<span data-ttu-id="755cb-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="755cb-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="755cb-128">-ServerName</span></span>
<span data-ttu-id="755cb-129">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-129">The name of the server.</span></span>

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

### <span data-ttu-id="755cb-130">-Source</span><span class="sxs-lookup"><span data-stu-id="755cb-130">-Source</span></span>
<span data-ttu-id="755cb-131">업데이트 값의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-131">The source of the updating value.</span></span>
<span data-ttu-id="755cb-132">기본값은 사용자 오버라이드입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-132">The default value is user-override</span></span>

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

### <span data-ttu-id="755cb-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="755cb-133">-SubscriptionId</span></span>
<span data-ttu-id="755cb-134">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="755cb-135">-Value</span><span class="sxs-lookup"><span data-stu-id="755cb-135">-Value</span></span>
<span data-ttu-id="755cb-136">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="755cb-137">-확인</span><span class="sxs-lookup"><span data-stu-id="755cb-137">-Confirm</span></span>
<span data-ttu-id="755cb-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755cb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755cb-139">-WhatIf</span></span>
<span data-ttu-id="755cb-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755cb-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755cb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755cb-142">CommonParameters</span></span>
<span data-ttu-id="755cb-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755cb-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="755cb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755cb-145">입력</span><span class="sxs-lookup"><span data-stu-id="755cb-145">INPUTS</span></span>

### <span data-ttu-id="755cb-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="755cb-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="755cb-147">출력</span><span class="sxs-lookup"><span data-stu-id="755cb-147">OUTPUTS</span></span>

### <span data-ttu-id="755cb-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="755cb-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="755cb-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="755cb-149">NOTES</span></span>

<span data-ttu-id="755cb-150">별칭</span><span class="sxs-lookup"><span data-stu-id="755cb-150">ALIASES</span></span>

<span data-ttu-id="755cb-151">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="755cb-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="755cb-152">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="755cb-153">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="755cb-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="755cb-154">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="755cb-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="755cb-155">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="755cb-156">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="755cb-157">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="755cb-158">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="755cb-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="755cb-159">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="755cb-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="755cb-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="755cb-162">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="755cb-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="755cb-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="755cb-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="755cb-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="755cb-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="755cb-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="755cb-167">RELATED LINKS</span></span>

