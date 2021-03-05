---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: e8367638f2bcfcf54f0b3183180f2ab8d70b3ffc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003920"
---
# <span data-ttu-id="d04bc-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d04bc-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="d04bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d04bc-103">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-103">Restarts a server.</span></span>

## <span data-ttu-id="d04bc-104">구문</span><span class="sxs-lookup"><span data-stu-id="d04bc-104">SYNTAX</span></span>

### <span data-ttu-id="d04bc-105">ServerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d04bc-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d04bc-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="d04bc-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d04bc-107">설명</span><span class="sxs-lookup"><span data-stu-id="d04bc-107">DESCRIPTION</span></span>
<span data-ttu-id="d04bc-108">서버를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-108">Restarts a server.</span></span>

## <span data-ttu-id="d04bc-109">예제</span><span class="sxs-lookup"><span data-stu-id="d04bc-109">EXAMPLES</span></span>

### <span data-ttu-id="d04bc-110">예제 1: MariaDB 다시 시작</span><span class="sxs-lookup"><span data-stu-id="d04bc-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="d04bc-111">이 명령은 MariaDB를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="d04bc-112">예제 2: MariaDB 다시 시작</span><span class="sxs-lookup"><span data-stu-id="d04bc-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="d04bc-113">이 명령은 MariaDB를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="d04bc-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d04bc-114">PARAMETERS</span></span>

### <span data-ttu-id="d04bc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d04bc-115">-AsJob</span></span>
<span data-ttu-id="d04bc-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d04bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04bc-117">-DefaultProfile</span></span>
<span data-ttu-id="d04bc-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04bc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d04bc-119">-InputObject</span></span>
<span data-ttu-id="d04bc-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d04bc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d04bc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d04bc-121">-Name</span></span>
<span data-ttu-id="d04bc-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-122">The name of the server.</span></span>

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

### <span data-ttu-id="d04bc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d04bc-123">-NoWait</span></span>
<span data-ttu-id="d04bc-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="d04bc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d04bc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d04bc-125">-PassThru</span></span>
<span data-ttu-id="d04bc-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d04bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="d04bc-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d04bc-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d04bc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d04bc-130">-SubscriptionId</span></span>
<span data-ttu-id="d04bc-131">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d04bc-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d04bc-132">-Confirm</span></span>
<span data-ttu-id="d04bc-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d04bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d04bc-134">-WhatIf</span></span>
<span data-ttu-id="d04bc-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d04bc-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d04bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04bc-137">CommonParameters</span></span>
<span data-ttu-id="d04bc-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04bc-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d04bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04bc-140">입력</span><span class="sxs-lookup"><span data-stu-id="d04bc-140">INPUTS</span></span>

### <span data-ttu-id="d04bc-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d04bc-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d04bc-142">출력</span><span class="sxs-lookup"><span data-stu-id="d04bc-142">OUTPUTS</span></span>

### <span data-ttu-id="d04bc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d04bc-143">System.Boolean</span></span>

## <span data-ttu-id="d04bc-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d04bc-144">NOTES</span></span>

<span data-ttu-id="d04bc-145">별칭</span><span class="sxs-lookup"><span data-stu-id="d04bc-145">ALIASES</span></span>

<span data-ttu-id="d04bc-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d04bc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d04bc-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d04bc-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d04bc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d04bc-149">INPUTOBJECT <IMariaDbIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d04bc-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d04bc-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d04bc-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d04bc-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d04bc-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d04bc-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d04bc-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d04bc-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d04bc-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d04bc-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d04bc-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d04bc-159">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d04bc-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d04bc-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d04bc-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d04bc-161">RELATED LINKS</span></span>

