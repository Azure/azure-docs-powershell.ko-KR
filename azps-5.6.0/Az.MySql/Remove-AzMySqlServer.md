---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: fee3eb40bdab571df4f1f2c0aa384f341c70d637
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011936"
---
# <span data-ttu-id="8ad17-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="8ad17-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="8ad17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad17-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad17-103">서버를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-103">Deletes a server.</span></span>

## <span data-ttu-id="8ad17-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ad17-104">SYNTAX</span></span>

### <span data-ttu-id="8ad17-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="8ad17-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ad17-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ad17-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ad17-107">설명</span><span class="sxs-lookup"><span data-stu-id="8ad17-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad17-108">서버를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-108">Deletes a server.</span></span>

## <span data-ttu-id="8ad17-109">예제</span><span class="sxs-lookup"><span data-stu-id="8ad17-109">EXAMPLES</span></span>

### <span data-ttu-id="8ad17-110">예제 1: resourceGroup 및 서버 이름으로 MySql 서버 제거</span><span class="sxs-lookup"><span data-stu-id="8ad17-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="8ad17-111">이 cmdlet은 resourceGroup 및 서버 이름으로 MySql 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="8ad17-112">예제 2: ID로 MySql 서버 제거</span><span class="sxs-lookup"><span data-stu-id="8ad17-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="8ad17-113">이러한 cmdlet은 ID로 MySql 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="8ad17-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ad17-114">PARAMETERS</span></span>

### <span data-ttu-id="8ad17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ad17-115">-AsJob</span></span>
<span data-ttu-id="8ad17-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8ad17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad17-117">-DefaultProfile</span></span>
<span data-ttu-id="8ad17-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ad17-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ad17-119">-InputObject</span></span>
<span data-ttu-id="8ad17-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8ad17-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ad17-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad17-121">-Name</span></span>
<span data-ttu-id="8ad17-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad17-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8ad17-123">-NoWait</span></span>
<span data-ttu-id="8ad17-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="8ad17-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8ad17-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ad17-125">-PassThru</span></span>
<span data-ttu-id="8ad17-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8ad17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad17-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ad17-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-128">The name of the resource group.</span></span>
<span data-ttu-id="8ad17-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8ad17-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ad17-130">-SubscriptionId</span></span>
<span data-ttu-id="8ad17-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8ad17-132">-확인</span><span class="sxs-lookup"><span data-stu-id="8ad17-132">-Confirm</span></span>
<span data-ttu-id="8ad17-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad17-134">-WhatIf</span></span>
<span data-ttu-id="8ad17-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ad17-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad17-137">CommonParameters</span></span>
<span data-ttu-id="8ad17-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad17-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ad17-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad17-140">입력</span><span class="sxs-lookup"><span data-stu-id="8ad17-140">INPUTS</span></span>

### <span data-ttu-id="8ad17-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8ad17-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8ad17-142">출력</span><span class="sxs-lookup"><span data-stu-id="8ad17-142">OUTPUTS</span></span>

### <span data-ttu-id="8ad17-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ad17-143">System.Boolean</span></span>

## <span data-ttu-id="8ad17-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ad17-144">NOTES</span></span>

<span data-ttu-id="8ad17-145">별칭</span><span class="sxs-lookup"><span data-stu-id="8ad17-145">ALIASES</span></span>

<span data-ttu-id="8ad17-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8ad17-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ad17-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ad17-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ad17-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ad17-149">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ad17-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ad17-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8ad17-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8ad17-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8ad17-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8ad17-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ad17-154">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8ad17-155">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8ad17-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8ad17-157">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="8ad17-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8ad17-159">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8ad17-160">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8ad17-161">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ad17-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8ad17-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ad17-162">RELATED LINKS</span></span>

