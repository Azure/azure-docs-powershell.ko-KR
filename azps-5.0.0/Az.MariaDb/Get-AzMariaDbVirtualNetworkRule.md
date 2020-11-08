---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218902"
---
# <span data-ttu-id="29a15-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29a15-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="29a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a15-102">SYNOPSIS</span></span>
<span data-ttu-id="29a15-103">가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="29a15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29a15-104">SYNTAX</span></span>

### <span data-ttu-id="29a15-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="29a15-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="29a15-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="29a15-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="29a15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="29a15-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="29a15-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29a15-108">DESCRIPTION</span></span>
<span data-ttu-id="29a15-109">가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="29a15-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29a15-110">EXAMPLES</span></span>

### <span data-ttu-id="29a15-111">예제 1: a 2의 모든 가상 네트워크 규칙 나열 (Adb)</span><span class="sxs-lookup"><span data-stu-id="29a15-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="29a15-112">이 명령은 모든 가상 네트워크 규칙을 그 아래에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="29a15-113">예제 2: 가상 네트워크 규칙을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="29a15-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="29a15-114">이 명령은 a 2 i의 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="29a15-115">변수</span><span class="sxs-lookup"><span data-stu-id="29a15-115">PARAMETERS</span></span>

### <span data-ttu-id="29a15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a15-116">-DefaultProfile</span></span>
<span data-ttu-id="29a15-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29a15-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29a15-118">-InputObject</span></span>
<span data-ttu-id="29a15-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29a15-120">-이름</span><span class="sxs-lookup"><span data-stu-id="29a15-120">-Name</span></span>
<span data-ttu-id="29a15-121">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a15-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29a15-122">-PassThru</span></span>
<span data-ttu-id="29a15-123">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="29a15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a15-124">-ResourceGroupName</span></span>
<span data-ttu-id="29a15-125">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="29a15-126">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a15-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29a15-127">-ServerName</span></span>
<span data-ttu-id="29a15-128">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a15-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29a15-129">-SubscriptionId</span></span>
<span data-ttu-id="29a15-130">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-130">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a15-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a15-131">CommonParameters</span></span>
<span data-ttu-id="29a15-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a15-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29a15-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a15-134">입력</span><span class="sxs-lookup"><span data-stu-id="29a15-134">INPUTS</span></span>

### <span data-ttu-id="29a15-135">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="29a15-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="29a15-136">출력</span><span class="sxs-lookup"><span data-stu-id="29a15-136">OUTPUTS</span></span>

### <span data-ttu-id="29a15-137">Microsoft. Api20180601Preview. IVirtualNetworkRule에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="29a15-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="29a15-138">상속자</span><span class="sxs-lookup"><span data-stu-id="29a15-138">NOTES</span></span>

<span data-ttu-id="29a15-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="29a15-139">ALIASES</span></span>

<span data-ttu-id="29a15-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="29a15-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29a15-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29a15-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="29a15-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29a15-143">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="29a15-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29a15-144">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="29a15-145">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="29a15-146">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="29a15-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="29a15-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29a15-148">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="29a15-149">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="29a15-150">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="29a15-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="29a15-152">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="29a15-153">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="29a15-154">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29a15-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="29a15-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29a15-155">RELATED LINKS</span></span>

