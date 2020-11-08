---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 86cc2a249479807adc14ad0faa4c682d1fef4725
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214411"
---
# <span data-ttu-id="7264a-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="7264a-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="7264a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7264a-102">SYNOPSIS</span></span>
<span data-ttu-id="7264a-103">서버를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-103">Deletes a server.</span></span>

## <span data-ttu-id="7264a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7264a-104">SYNTAX</span></span>

### <span data-ttu-id="7264a-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7264a-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7264a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7264a-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7264a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7264a-107">DESCRIPTION</span></span>
<span data-ttu-id="7264a-108">서버를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-108">Deletes a server.</span></span>

## <span data-ttu-id="7264a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7264a-109">EXAMPLES</span></span>

### <span data-ttu-id="7264a-110">예제 1: 리소스 및 서버 이름으로 MySql 서버 제거</span><span class="sxs-lookup"><span data-stu-id="7264a-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="7264a-111">이 cmdlet은 리소스 및 서버 이름으로 MySql 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="7264a-112">예제 2: id로 MySql 서버 제거</span><span class="sxs-lookup"><span data-stu-id="7264a-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="7264a-113">이러한 cmdlet은 id로 MySql 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="7264a-114">변수</span><span class="sxs-lookup"><span data-stu-id="7264a-114">PARAMETERS</span></span>

### <span data-ttu-id="7264a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7264a-115">-AsJob</span></span>
<span data-ttu-id="7264a-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="7264a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7264a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7264a-117">-DefaultProfile</span></span>
<span data-ttu-id="7264a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7264a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7264a-119">-InputObject</span></span>
<span data-ttu-id="7264a-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7264a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7264a-121">-Name</span></span>
<span data-ttu-id="7264a-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-122">The name of the server.</span></span>

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

### <span data-ttu-id="7264a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7264a-123">-NoWait</span></span>
<span data-ttu-id="7264a-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="7264a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7264a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7264a-125">-PassThru</span></span>
<span data-ttu-id="7264a-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7264a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7264a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7264a-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-128">The name of the resource group.</span></span>
<span data-ttu-id="7264a-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7264a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7264a-130">-SubscriptionId</span></span>
<span data-ttu-id="7264a-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7264a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7264a-132">-Confirm</span></span>
<span data-ttu-id="7264a-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7264a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7264a-134">-WhatIf</span></span>
<span data-ttu-id="7264a-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7264a-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7264a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7264a-137">CommonParameters</span></span>
<span data-ttu-id="7264a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7264a-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7264a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7264a-140">입력</span><span class="sxs-lookup"><span data-stu-id="7264a-140">INPUTS</span></span>

### <span data-ttu-id="7264a-141">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="7264a-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7264a-142">출력</span><span class="sxs-lookup"><span data-stu-id="7264a-142">OUTPUTS</span></span>

### <span data-ttu-id="7264a-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7264a-143">System.Boolean</span></span>

## <span data-ttu-id="7264a-144">상속자</span><span class="sxs-lookup"><span data-stu-id="7264a-144">NOTES</span></span>

<span data-ttu-id="7264a-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="7264a-145">ALIASES</span></span>

<span data-ttu-id="7264a-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7264a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7264a-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7264a-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7264a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7264a-149">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7264a-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7264a-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7264a-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7264a-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7264a-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="7264a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7264a-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7264a-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7264a-156">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="7264a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7264a-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7264a-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7264a-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7264a-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7264a-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7264a-161">RELATED LINKS</span></span>

