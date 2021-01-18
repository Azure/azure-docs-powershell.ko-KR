---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492812"
---
# <span data-ttu-id="b7917-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="b7917-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="b7917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7917-102">SYNOPSIS</span></span>
<span data-ttu-id="b7917-103">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-103">Restarts a server.</span></span>

## <span data-ttu-id="b7917-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7917-104">SYNTAX</span></span>

### <span data-ttu-id="b7917-105">ServerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7917-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7917-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="b7917-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7917-107">설명</span><span class="sxs-lookup"><span data-stu-id="b7917-107">DESCRIPTION</span></span>
<span data-ttu-id="b7917-108">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-108">Restarts a server.</span></span>

## <span data-ttu-id="b7917-109">예제</span><span class="sxs-lookup"><span data-stu-id="b7917-109">EXAMPLES</span></span>

### <span data-ttu-id="b7917-110">예제 1: MariaDB 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b7917-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="b7917-111">이 명령은 MariaDB를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="b7917-112">예제 2: MariaDB 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b7917-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="b7917-113">이 명령은 MariaDB를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="b7917-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7917-114">PARAMETERS</span></span>

### <span data-ttu-id="b7917-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7917-115">-AsJob</span></span>
<span data-ttu-id="b7917-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b7917-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b7917-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7917-117">-DefaultProfile</span></span>
<span data-ttu-id="b7917-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7917-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7917-119">-InputObject</span></span>
<span data-ttu-id="b7917-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b7917-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7917-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b7917-121">-Name</span></span>
<span data-ttu-id="b7917-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7917-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b7917-123">-NoWait</span></span>
<span data-ttu-id="b7917-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="b7917-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b7917-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7917-125">-PassThru</span></span>
<span data-ttu-id="b7917-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b7917-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7917-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7917-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b7917-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7917-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7917-130">-SubscriptionId</span></span>
<span data-ttu-id="b7917-131">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7917-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7917-132">-Confirm</span></span>
<span data-ttu-id="b7917-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7917-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7917-134">-WhatIf</span></span>
<span data-ttu-id="b7917-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b7917-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7917-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7917-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7917-137">CommonParameters</span></span>
<span data-ttu-id="b7917-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7917-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7917-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7917-140">입력</span><span class="sxs-lookup"><span data-stu-id="b7917-140">INPUTS</span></span>

### <span data-ttu-id="b7917-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="b7917-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b7917-142">출력</span><span class="sxs-lookup"><span data-stu-id="b7917-142">OUTPUTS</span></span>

### <span data-ttu-id="b7917-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7917-143">System.Boolean</span></span>

## <span data-ttu-id="b7917-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7917-144">NOTES</span></span>

<span data-ttu-id="b7917-145">별칭</span><span class="sxs-lookup"><span data-stu-id="b7917-145">ALIASES</span></span>

<span data-ttu-id="b7917-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b7917-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7917-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7917-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7917-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7917-149">INPUTOBJECT: <IMariaDbIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7917-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7917-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b7917-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b7917-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b7917-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b7917-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7917-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b7917-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b7917-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b7917-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b7917-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b7917-159">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b7917-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7917-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b7917-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7917-161">RELATED LINKS</span></span>

