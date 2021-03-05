---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 931b808838503ab6bf481225e6f5994326ef8319
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997794"
---
# <span data-ttu-id="e04cd-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="e04cd-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="e04cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e04cd-103">데이터베이스 주체 사용 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="e04cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="e04cd-104">SYNTAX</span></span>

### <span data-ttu-id="e04cd-105">RemoveExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e04cd-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e04cd-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e04cd-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e04cd-107">설명</span><span class="sxs-lookup"><span data-stu-id="e04cd-107">DESCRIPTION</span></span>
<span data-ttu-id="e04cd-108">데이터베이스 주체 사용 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="e04cd-109">예제</span><span class="sxs-lookup"><span data-stu-id="e04cd-109">EXAMPLES</span></span>

### <span data-ttu-id="e04cd-110">예제 1: 데이터베이스 주체 권한 제거</span><span class="sxs-lookup"><span data-stu-id="e04cd-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="e04cd-111">위의 명령은 데이터베이스 주체 사용 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="e04cd-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e04cd-112">PARAMETERS</span></span>

### <span data-ttu-id="e04cd-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e04cd-113">-ClusterName</span></span>
<span data-ttu-id="e04cd-114">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04cd-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e04cd-115">-DatabaseName</span></span>
<span data-ttu-id="e04cd-116">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04cd-117">-DefaultProfile</span></span>
<span data-ttu-id="e04cd-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e04cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e04cd-119">-InputObject</span></span>
<span data-ttu-id="e04cd-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e04cd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e04cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="e04cd-122">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04cd-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e04cd-123">-SubscriptionId</span></span>
<span data-ttu-id="e04cd-124">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e04cd-125">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04cd-126">-Value</span><span class="sxs-lookup"><span data-stu-id="e04cd-126">-Value</span></span>
<span data-ttu-id="e04cd-127">Kusto 데이터베이스 주체 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="e04cd-128">생성을 위해 VALUE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e04cd-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04cd-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e04cd-129">-Confirm</span></span>
<span data-ttu-id="e04cd-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04cd-131">-WhatIf</span></span>
<span data-ttu-id="e04cd-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e04cd-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e04cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04cd-134">CommonParameters</span></span>
<span data-ttu-id="e04cd-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04cd-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e04cd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04cd-137">입력</span><span class="sxs-lookup"><span data-stu-id="e04cd-137">INPUTS</span></span>

### <span data-ttu-id="e04cd-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e04cd-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e04cd-139">출력</span><span class="sxs-lookup"><span data-stu-id="e04cd-139">OUTPUTS</span></span>

### <span data-ttu-id="e04cd-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="e04cd-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="e04cd-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e04cd-141">NOTES</span></span>

<span data-ttu-id="e04cd-142">별칭</span><span class="sxs-lookup"><span data-stu-id="e04cd-142">ALIASES</span></span>

<span data-ttu-id="e04cd-143">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e04cd-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e04cd-144">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e04cd-145">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e04cd-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e04cd-146">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e04cd-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e04cd-147">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e04cd-148">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e04cd-149">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e04cd-150">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e04cd-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e04cd-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e04cd-152">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e04cd-153">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e04cd-154">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e04cd-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e04cd-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e04cd-157">VALUE <IDatabasePrincipal[]>: Kusto 데이터베이스 주체 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="e04cd-158">`Name <String>`: 데이터베이스 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="e04cd-159">`Role <DatabasePrincipalRole>`: 데이터베이스 주체 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="e04cd-160">`Type <DatabasePrincipalType>`: 데이터베이스 주체 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="e04cd-161">`[AppId <String>]`: 애플리케이션 ID - 애플리케이션 주체 유형에만 관련됩니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="e04cd-162">`[Email <String>]`: 데이터베이스 주체 전자 메일이 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="e04cd-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="e04cd-163">`[Fqn <String>]`: 데이터베이스 주체가 완전히 자격을 갖춘 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e04cd-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="e04cd-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e04cd-164">RELATED LINKS</span></span>

