---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/stop-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d51946f9d358a7a7ccffff5e4621248d7c89fa9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953568"
---
# <span data-ttu-id="03fc8-101">Stop-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="03fc8-101">Stop-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="03fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="03fc8-103">서버를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-103">Stops a server.</span></span>

## <span data-ttu-id="03fc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="03fc8-104">SYNTAX</span></span>

### <span data-ttu-id="03fc8-105">중지(기본값)</span><span class="sxs-lookup"><span data-stu-id="03fc8-105">Stop (Default)</span></span>
```
Stop-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03fc8-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03fc8-106">StopViaIdentity</span></span>
```
Stop-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03fc8-107">설명</span><span class="sxs-lookup"><span data-stu-id="03fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="03fc8-108">서버를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-108">Stops a server.</span></span>

## <span data-ttu-id="03fc8-109">예제</span><span class="sxs-lookup"><span data-stu-id="03fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="03fc8-110">예제 1: 리소스 이름으로 서버를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="03fc8-111">이름으로 서버 중지</span><span class="sxs-lookup"><span data-stu-id="03fc8-111">Stop the server by name</span></span>

### <span data-ttu-id="03fc8-112">예제 2: ID로 서버 중지</span><span class="sxs-lookup"><span data-stu-id="03fc8-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/stop"
PS C:\> Stop-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="03fc8-113">ID로 서버 중지</span><span class="sxs-lookup"><span data-stu-id="03fc8-113">Stop the server by identity</span></span>

## <span data-ttu-id="03fc8-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03fc8-114">PARAMETERS</span></span>

### <span data-ttu-id="03fc8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03fc8-115">-AsJob</span></span>
<span data-ttu-id="03fc8-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="03fc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fc8-117">-DefaultProfile</span></span>
<span data-ttu-id="03fc8-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fc8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03fc8-119">-InputObject</span></span>
<span data-ttu-id="03fc8-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="03fc8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03fc8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="03fc8-121">-Name</span></span>
<span data-ttu-id="03fc8-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="03fc8-123">-NoWait</span></span>
<span data-ttu-id="03fc8-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="03fc8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="03fc8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03fc8-125">-PassThru</span></span>
<span data-ttu-id="03fc8-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="03fc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="03fc8-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-128">The name of the resource group.</span></span>
<span data-ttu-id="03fc8-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03fc8-130">-SubscriptionId</span></span>
<span data-ttu-id="03fc8-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fc8-132">-확인</span><span class="sxs-lookup"><span data-stu-id="03fc8-132">-Confirm</span></span>
<span data-ttu-id="03fc8-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fc8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fc8-134">-WhatIf</span></span>
<span data-ttu-id="03fc8-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fc8-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fc8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fc8-137">CommonParameters</span></span>
<span data-ttu-id="03fc8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fc8-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03fc8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fc8-140">입력</span><span class="sxs-lookup"><span data-stu-id="03fc8-140">INPUTS</span></span>

### <span data-ttu-id="03fc8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="03fc8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="03fc8-142">출력</span><span class="sxs-lookup"><span data-stu-id="03fc8-142">OUTPUTS</span></span>

### <span data-ttu-id="03fc8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03fc8-143">System.Boolean</span></span>

## <span data-ttu-id="03fc8-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03fc8-144">NOTES</span></span>

<span data-ttu-id="03fc8-145">별칭</span><span class="sxs-lookup"><span data-stu-id="03fc8-145">ALIASES</span></span>

<span data-ttu-id="03fc8-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="03fc8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03fc8-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03fc8-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03fc8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03fc8-149">INPUTOBJECT <IPostgreSqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="03fc8-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03fc8-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="03fc8-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="03fc8-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="03fc8-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="03fc8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03fc8-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="03fc8-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="03fc8-156">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="03fc8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="03fc8-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="03fc8-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="03fc8-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03fc8-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="03fc8-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03fc8-161">RELATED LINKS</span></span>

