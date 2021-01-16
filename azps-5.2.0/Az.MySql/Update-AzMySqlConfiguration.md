---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360263"
---
# <span data-ttu-id="28f55-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="28f55-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="28f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28f55-102">SYNOPSIS</span></span>
<span data-ttu-id="28f55-103">서버의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="28f55-104">AdministratorLoginPassword, Update-AzMySqlServer 업데이트하려는 경우 대신 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="28f55-105">구문</span><span class="sxs-lookup"><span data-stu-id="28f55-105">SYNTAX</span></span>

### <span data-ttu-id="28f55-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="28f55-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28f55-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="28f55-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28f55-108">설명</span><span class="sxs-lookup"><span data-stu-id="28f55-108">DESCRIPTION</span></span>
<span data-ttu-id="28f55-109">서버의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="28f55-110">AdministratorLoginPassword, Update-AzMySqlServer 업데이트하려는 경우 대신 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="28f55-111">예제</span><span class="sxs-lookup"><span data-stu-id="28f55-111">EXAMPLES</span></span>

### <span data-ttu-id="28f55-112">예제 1: 이름으로 MySql 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="28f55-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="28f55-113">이 cmdlet은 이름으로 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="28f55-114">예제 2: ID로 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="28f55-115">이러한 cmdlet은 ID에 따라 MySql 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="28f55-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28f55-116">PARAMETERS</span></span>

### <span data-ttu-id="28f55-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28f55-117">-AsJob</span></span>
<span data-ttu-id="28f55-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="28f55-118">Run the command as a job</span></span>

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

### <span data-ttu-id="28f55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f55-119">-DefaultProfile</span></span>
<span data-ttu-id="28f55-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28f55-121">-InputObject</span></span>
<span data-ttu-id="28f55-122">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-122">Identity Parameter.</span></span>
<span data-ttu-id="28f55-123">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="28f55-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="28f55-124">-Name</span><span class="sxs-lookup"><span data-stu-id="28f55-124">-Name</span></span>
<span data-ttu-id="28f55-125">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="28f55-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="28f55-126">-NoWait</span></span>
<span data-ttu-id="28f55-127">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="28f55-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="28f55-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f55-128">-ResourceGroupName</span></span>
<span data-ttu-id="28f55-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-129">The name of the resource group.</span></span>
<span data-ttu-id="28f55-130">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="28f55-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28f55-131">-ServerName</span></span>
<span data-ttu-id="28f55-132">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-132">The name of the server.</span></span>

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

### <span data-ttu-id="28f55-133">-Source</span><span class="sxs-lookup"><span data-stu-id="28f55-133">-Source</span></span>
<span data-ttu-id="28f55-134">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="28f55-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28f55-135">-SubscriptionId</span></span>
<span data-ttu-id="28f55-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="28f55-137">-Value</span><span class="sxs-lookup"><span data-stu-id="28f55-137">-Value</span></span>
<span data-ttu-id="28f55-138">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="28f55-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28f55-139">-Confirm</span></span>
<span data-ttu-id="28f55-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28f55-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f55-141">-WhatIf</span></span>
<span data-ttu-id="28f55-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28f55-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28f55-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28f55-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f55-144">CommonParameters</span></span>
<span data-ttu-id="28f55-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f55-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28f55-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f55-147">입력</span><span class="sxs-lookup"><span data-stu-id="28f55-147">INPUTS</span></span>

### <span data-ttu-id="28f55-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="28f55-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="28f55-149">출력</span><span class="sxs-lookup"><span data-stu-id="28f55-149">OUTPUTS</span></span>

### <span data-ttu-id="28f55-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="28f55-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="28f55-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28f55-151">NOTES</span></span>

<span data-ttu-id="28f55-152">별칭</span><span class="sxs-lookup"><span data-stu-id="28f55-152">ALIASES</span></span>

<span data-ttu-id="28f55-153">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="28f55-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28f55-154">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28f55-155">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28f55-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28f55-156">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="28f55-157">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="28f55-158">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="28f55-159">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="28f55-160">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="28f55-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28f55-161">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="28f55-162">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="28f55-163">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="28f55-164">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="28f55-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="28f55-166">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="28f55-167">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="28f55-168">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28f55-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="28f55-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28f55-169">RELATED LINKS</span></span>

