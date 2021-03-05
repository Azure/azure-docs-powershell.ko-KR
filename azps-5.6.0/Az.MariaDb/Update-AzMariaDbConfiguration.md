---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: dc2a36a9ac8c2595ef2f60b8edc40582ad864ff8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003888"
---
# <span data-ttu-id="4a252-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a252-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="4a252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a252-102">SYNOPSIS</span></span>
<span data-ttu-id="4a252-103">서버 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="4a252-104">AdministratorLoginPassword, sku 등을 업데이트하려는 경우 대신 Update-AzMariaDbServer 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="4a252-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4a252-105">구문</span><span class="sxs-lookup"><span data-stu-id="4a252-105">SYNTAX</span></span>

### <span data-ttu-id="4a252-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="4a252-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a252-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4a252-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a252-108">설명</span><span class="sxs-lookup"><span data-stu-id="4a252-108">DESCRIPTION</span></span>
<span data-ttu-id="4a252-109">서버 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="4a252-110">AdministratorLoginPassword, sku 등을 업데이트하려는 경우 대신 Update-AzMariaDberver 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="4a252-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="4a252-111">예제</span><span class="sxs-lookup"><span data-stu-id="4a252-111">EXAMPLES</span></span>

### <span data-ttu-id="4a252-112">예제 1: MariaDB 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="4a252-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="4a252-113">이 명령은 MariaDB 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="4a252-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a252-114">PARAMETERS</span></span>

### <span data-ttu-id="4a252-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a252-115">-AsJob</span></span>
<span data-ttu-id="4a252-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4a252-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a252-117">-DefaultProfile</span></span>
<span data-ttu-id="4a252-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a252-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a252-119">-InputObject</span></span>
<span data-ttu-id="4a252-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4a252-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a252-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4a252-121">-Name</span></span>
<span data-ttu-id="4a252-122">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4a252-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a252-123">-NoWait</span></span>
<span data-ttu-id="4a252-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="4a252-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a252-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a252-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a252-126">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4a252-127">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4a252-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a252-128">-ServerName</span></span>
<span data-ttu-id="4a252-129">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-129">The name of the server.</span></span>

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

### <span data-ttu-id="4a252-130">-Source</span><span class="sxs-lookup"><span data-stu-id="4a252-130">-Source</span></span>
<span data-ttu-id="4a252-131">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="4a252-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a252-132">-SubscriptionId</span></span>
<span data-ttu-id="4a252-133">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4a252-134">-Value</span><span class="sxs-lookup"><span data-stu-id="4a252-134">-Value</span></span>
<span data-ttu-id="4a252-135">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="4a252-136">-확인</span><span class="sxs-lookup"><span data-stu-id="4a252-136">-Confirm</span></span>
<span data-ttu-id="4a252-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a252-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a252-138">-WhatIf</span></span>
<span data-ttu-id="4a252-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a252-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a252-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a252-141">CommonParameters</span></span>
<span data-ttu-id="4a252-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a252-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a252-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a252-144">입력</span><span class="sxs-lookup"><span data-stu-id="4a252-144">INPUTS</span></span>

### <span data-ttu-id="4a252-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4a252-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4a252-146">출력</span><span class="sxs-lookup"><span data-stu-id="4a252-146">OUTPUTS</span></span>

### <span data-ttu-id="4a252-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a252-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="4a252-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a252-148">NOTES</span></span>

<span data-ttu-id="4a252-149">별칭</span><span class="sxs-lookup"><span data-stu-id="4a252-149">ALIASES</span></span>

<span data-ttu-id="4a252-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4a252-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a252-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a252-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a252-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a252-153">INPUTOBJECT <IMariaDbIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a252-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a252-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4a252-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4a252-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4a252-157">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4a252-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a252-158">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4a252-159">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4a252-160">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4a252-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4a252-162">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4a252-163">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4a252-164">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a252-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4a252-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a252-165">RELATED LINKS</span></span>

