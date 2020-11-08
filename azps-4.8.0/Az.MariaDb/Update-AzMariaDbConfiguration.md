---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213526"
---
# <span data-ttu-id="20f5c-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f5c-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="20f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="20f5c-103">서버 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="20f5c-104">AdministratorLoginPassword, sku 등을 업데이트 하려는 경우 대신 Update-AzMariaDbServer를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="20f5c-105">구문과</span><span class="sxs-lookup"><span data-stu-id="20f5c-105">SYNTAX</span></span>

### <span data-ttu-id="20f5c-106">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="20f5c-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20f5c-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="20f5c-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20f5c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="20f5c-108">DESCRIPTION</span></span>
<span data-ttu-id="20f5c-109">서버 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="20f5c-110">AdministratorLoginPassword, sku 등을 업데이트 하려는 경우 대신 Update-AzMariaDberver를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="20f5c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="20f5c-111">EXAMPLES</span></span>

### <span data-ttu-id="20f5c-112">예제 1:이 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="20f5c-113">이 명령은이을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="20f5c-114">변수</span><span class="sxs-lookup"><span data-stu-id="20f5c-114">PARAMETERS</span></span>

### <span data-ttu-id="20f5c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20f5c-115">-AsJob</span></span>
<span data-ttu-id="20f5c-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="20f5c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="20f5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f5c-117">-DefaultProfile</span></span>
<span data-ttu-id="20f5c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f5c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20f5c-119">-InputObject</span></span>
<span data-ttu-id="20f5c-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20f5c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="20f5c-121">-Name</span></span>
<span data-ttu-id="20f5c-122">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="20f5c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="20f5c-123">-NoWait</span></span>
<span data-ttu-id="20f5c-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="20f5c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="20f5c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f5c-125">-ResourceGroupName</span></span>
<span data-ttu-id="20f5c-126">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="20f5c-127">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="20f5c-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20f5c-128">-ServerName</span></span>
<span data-ttu-id="20f5c-129">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-129">The name of the server.</span></span>

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

### <span data-ttu-id="20f5c-130">-원본</span><span class="sxs-lookup"><span data-stu-id="20f5c-130">-Source</span></span>
<span data-ttu-id="20f5c-131">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="20f5c-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20f5c-132">-SubscriptionId</span></span>
<span data-ttu-id="20f5c-133">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="20f5c-134">-값</span><span class="sxs-lookup"><span data-stu-id="20f5c-134">-Value</span></span>
<span data-ttu-id="20f5c-135">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="20f5c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="20f5c-136">-Confirm</span></span>
<span data-ttu-id="20f5c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f5c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f5c-138">-WhatIf</span></span>
<span data-ttu-id="20f5c-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f5c-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f5c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f5c-141">CommonParameters</span></span>
<span data-ttu-id="20f5c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f5c-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20f5c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f5c-144">입력</span><span class="sxs-lookup"><span data-stu-id="20f5c-144">INPUTS</span></span>

### <span data-ttu-id="20f5c-145">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="20f5c-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="20f5c-146">출력</span><span class="sxs-lookup"><span data-stu-id="20f5c-146">OUTPUTS</span></span>

### <span data-ttu-id="20f5c-147">Microsoft. Api20180601Preview. IConfiguration에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="20f5c-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="20f5c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="20f5c-148">NOTES</span></span>

<span data-ttu-id="20f5c-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="20f5c-149">ALIASES</span></span>

<span data-ttu-id="20f5c-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="20f5c-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20f5c-151">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20f5c-152">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="20f5c-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20f5c-153">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="20f5c-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20f5c-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="20f5c-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="20f5c-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="20f5c-157">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="20f5c-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20f5c-158">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="20f5c-159">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="20f5c-160">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="20f5c-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="20f5c-162">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="20f5c-163">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="20f5c-164">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20f5c-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="20f5c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20f5c-165">RELATED LINKS</span></span>

