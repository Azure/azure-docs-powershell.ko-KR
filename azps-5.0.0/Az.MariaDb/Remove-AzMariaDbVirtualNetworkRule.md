---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218640"
---
# <span data-ttu-id="0a014-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0a014-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="0a014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a014-102">SYNOPSIS</span></span>
<span data-ttu-id="0a014-103">지정 된 이름의 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="0a014-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a014-104">SYNTAX</span></span>

### <span data-ttu-id="0a014-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a014-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0a014-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a014-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a014-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0a014-107">DESCRIPTION</span></span>
<span data-ttu-id="0a014-108">지정 된 이름의 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="0a014-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0a014-109">EXAMPLES</span></span>

### <span data-ttu-id="0a014-110">예제 1: 가상 네트워크 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="0a014-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="0a014-111">이 명령은 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="0a014-112">변수</span><span class="sxs-lookup"><span data-stu-id="0a014-112">PARAMETERS</span></span>

### <span data-ttu-id="0a014-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a014-113">-AsJob</span></span>
<span data-ttu-id="0a014-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="0a014-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0a014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a014-115">-DefaultProfile</span></span>
<span data-ttu-id="0a014-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a014-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a014-117">-InputObject</span></span>
<span data-ttu-id="0a014-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a014-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0a014-119">-Name</span></span>
<span data-ttu-id="0a014-120">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-120">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a014-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a014-121">-NoWait</span></span>
<span data-ttu-id="0a014-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="0a014-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a014-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a014-123">-PassThru</span></span>
<span data-ttu-id="0a014-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0a014-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a014-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a014-126">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0a014-127">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0a014-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a014-128">-ServerName</span></span>
<span data-ttu-id="0a014-129">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-129">The name of the server.</span></span>

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

### <span data-ttu-id="0a014-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a014-130">-SubscriptionId</span></span>
<span data-ttu-id="0a014-131">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0a014-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0a014-132">-Confirm</span></span>
<span data-ttu-id="0a014-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a014-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a014-134">-WhatIf</span></span>
<span data-ttu-id="0a014-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a014-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a014-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a014-137">CommonParameters</span></span>
<span data-ttu-id="0a014-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a014-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a014-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a014-140">입력</span><span class="sxs-lookup"><span data-stu-id="0a014-140">INPUTS</span></span>

### <span data-ttu-id="0a014-141">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="0a014-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="0a014-142">출력</span><span class="sxs-lookup"><span data-stu-id="0a014-142">OUTPUTS</span></span>

### <span data-ttu-id="0a014-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0a014-143">System.Boolean</span></span>

## <span data-ttu-id="0a014-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0a014-144">NOTES</span></span>

<span data-ttu-id="0a014-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="0a014-145">ALIASES</span></span>

<span data-ttu-id="0a014-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0a014-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a014-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a014-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a014-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a014-149">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0a014-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a014-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0a014-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0a014-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0a014-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="0a014-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a014-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0a014-155">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0a014-156">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0a014-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0a014-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0a014-159">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="0a014-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a014-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0a014-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a014-161">RELATED LINKS</span></span>

