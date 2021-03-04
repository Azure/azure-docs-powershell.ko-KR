---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9f2fbae69d2831d063ea6bfa92e2f1ece90e9f12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956112"
---
# <span data-ttu-id="86f20-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="86f20-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="86f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f20-102">SYNOPSIS</span></span>
<span data-ttu-id="86f20-103">데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-103">Deletes a database.</span></span>

## <span data-ttu-id="86f20-104">구문</span><span class="sxs-lookup"><span data-stu-id="86f20-104">SYNTAX</span></span>

### <span data-ttu-id="86f20-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="86f20-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="86f20-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86f20-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86f20-107">설명</span><span class="sxs-lookup"><span data-stu-id="86f20-107">DESCRIPTION</span></span>
<span data-ttu-id="86f20-108">데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-108">Deletes a database.</span></span>

## <span data-ttu-id="86f20-109">예제</span><span class="sxs-lookup"><span data-stu-id="86f20-109">EXAMPLES</span></span>

### <span data-ttu-id="86f20-110">예제 1: 이름에 따라 MySql 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="86f20-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="86f20-111">이 cmdlet은 이름으로 MySql 데이터베이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="86f20-112">예제 2: ID로 MySql 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="86f20-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="86f20-113">이러한 cmdlet은 ID로 MySql 데이터베이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="86f20-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="86f20-114">PARAMETERS</span></span>

### <span data-ttu-id="86f20-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86f20-115">-AsJob</span></span>
<span data-ttu-id="86f20-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-116">Run the command as a job</span></span>

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

### <span data-ttu-id="86f20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f20-117">-DefaultProfile</span></span>
<span data-ttu-id="86f20-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86f20-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86f20-119">-InputObject</span></span>
<span data-ttu-id="86f20-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86f20-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86f20-121">-Name</span><span class="sxs-lookup"><span data-stu-id="86f20-121">-Name</span></span>
<span data-ttu-id="86f20-122">데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-122">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f20-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="86f20-123">-NoWait</span></span>
<span data-ttu-id="86f20-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="86f20-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="86f20-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86f20-125">-PassThru</span></span>
<span data-ttu-id="86f20-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="86f20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f20-127">-ResourceGroupName</span></span>
<span data-ttu-id="86f20-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-128">The name of the resource group.</span></span>
<span data-ttu-id="86f20-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f20-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86f20-130">-ServerName</span></span>
<span data-ttu-id="86f20-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f20-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86f20-132">-SubscriptionId</span></span>
<span data-ttu-id="86f20-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f20-134">-확인</span><span class="sxs-lookup"><span data-stu-id="86f20-134">-Confirm</span></span>
<span data-ttu-id="86f20-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f20-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f20-136">-WhatIf</span></span>
<span data-ttu-id="86f20-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86f20-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f20-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f20-139">CommonParameters</span></span>
<span data-ttu-id="86f20-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f20-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86f20-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f20-142">입력</span><span class="sxs-lookup"><span data-stu-id="86f20-142">INPUTS</span></span>

### <span data-ttu-id="86f20-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="86f20-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="86f20-144">출력</span><span class="sxs-lookup"><span data-stu-id="86f20-144">OUTPUTS</span></span>

### <span data-ttu-id="86f20-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86f20-145">System.Boolean</span></span>

## <span data-ttu-id="86f20-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86f20-146">NOTES</span></span>

<span data-ttu-id="86f20-147">별칭</span><span class="sxs-lookup"><span data-stu-id="86f20-147">ALIASES</span></span>

<span data-ttu-id="86f20-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="86f20-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86f20-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86f20-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86f20-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86f20-151">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="86f20-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86f20-152">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="86f20-153">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="86f20-154">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="86f20-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="86f20-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86f20-156">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="86f20-157">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="86f20-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="86f20-159">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="86f20-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="86f20-161">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="86f20-162">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="86f20-163">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86f20-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="86f20-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86f20-164">RELATED LINKS</span></span>

