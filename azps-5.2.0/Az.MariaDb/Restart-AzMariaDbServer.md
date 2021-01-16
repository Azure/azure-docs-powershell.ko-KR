---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326731"
---
# <span data-ttu-id="578fd-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="578fd-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="578fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578fd-102">SYNOPSIS</span></span>
<span data-ttu-id="578fd-103">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-103">Restarts a server.</span></span>

## <span data-ttu-id="578fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="578fd-104">SYNTAX</span></span>

### <span data-ttu-id="578fd-105">ServerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="578fd-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="578fd-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="578fd-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="578fd-107">설명</span><span class="sxs-lookup"><span data-stu-id="578fd-107">DESCRIPTION</span></span>
<span data-ttu-id="578fd-108">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-108">Restarts a server.</span></span>

## <span data-ttu-id="578fd-109">예제</span><span class="sxs-lookup"><span data-stu-id="578fd-109">EXAMPLES</span></span>

### <span data-ttu-id="578fd-110">예제 1: MariaDB 다시 시작</span><span class="sxs-lookup"><span data-stu-id="578fd-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="578fd-111">이 명령은 MariaDB를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="578fd-112">예제 2: MariaDB 다시 시작</span><span class="sxs-lookup"><span data-stu-id="578fd-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="578fd-113">이 명령은 MariaDB를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="578fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="578fd-114">PARAMETERS</span></span>

### <span data-ttu-id="578fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="578fd-115">-AsJob</span></span>
<span data-ttu-id="578fd-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="578fd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="578fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578fd-117">-DefaultProfile</span></span>
<span data-ttu-id="578fd-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578fd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="578fd-119">-InputObject</span></span>
<span data-ttu-id="578fd-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="578fd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="578fd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="578fd-121">-Name</span></span>
<span data-ttu-id="578fd-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-122">The name of the server.</span></span>

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

### <span data-ttu-id="578fd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="578fd-123">-NoWait</span></span>
<span data-ttu-id="578fd-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="578fd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="578fd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="578fd-125">-PassThru</span></span>
<span data-ttu-id="578fd-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="578fd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578fd-127">-ResourceGroupName</span></span>
<span data-ttu-id="578fd-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="578fd-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="578fd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="578fd-130">-SubscriptionId</span></span>
<span data-ttu-id="578fd-131">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="578fd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="578fd-132">-Confirm</span></span>
<span data-ttu-id="578fd-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578fd-134">-WhatIf</span></span>
<span data-ttu-id="578fd-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="578fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578fd-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578fd-137">CommonParameters</span></span>
<span data-ttu-id="578fd-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578fd-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="578fd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578fd-140">입력</span><span class="sxs-lookup"><span data-stu-id="578fd-140">INPUTS</span></span>

### <span data-ttu-id="578fd-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="578fd-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="578fd-142">출력</span><span class="sxs-lookup"><span data-stu-id="578fd-142">OUTPUTS</span></span>

### <span data-ttu-id="578fd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="578fd-143">System.Boolean</span></span>

## <span data-ttu-id="578fd-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="578fd-144">NOTES</span></span>

<span data-ttu-id="578fd-145">별칭</span><span class="sxs-lookup"><span data-stu-id="578fd-145">ALIASES</span></span>

<span data-ttu-id="578fd-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="578fd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="578fd-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="578fd-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="578fd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="578fd-149">INPUTOBJECT: <IMariaDbIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="578fd-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="578fd-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="578fd-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="578fd-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="578fd-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="578fd-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="578fd-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="578fd-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="578fd-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="578fd-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="578fd-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="578fd-159">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="578fd-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fd-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="578fd-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="578fd-161">RELATED LINKS</span></span>

