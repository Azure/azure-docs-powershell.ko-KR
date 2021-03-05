---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: 9be95744e7528a1b1eeec3a2784e7c0ccf21e8d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965872"
---
# <span data-ttu-id="59da7-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="59da7-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="59da7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59da7-102">SYNOPSIS</span></span>
<span data-ttu-id="59da7-103">데이터베이스 이름이 유효하고 아직 사용되지 않는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="59da7-104">구문</span><span class="sxs-lookup"><span data-stu-id="59da7-104">SYNTAX</span></span>

### <span data-ttu-id="59da7-105">CheckExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="59da7-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="59da7-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="59da7-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59da7-107">설명</span><span class="sxs-lookup"><span data-stu-id="59da7-107">DESCRIPTION</span></span>
<span data-ttu-id="59da7-108">데이터베이스 이름이 유효하고 아직 사용되지 않는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="59da7-109">예제</span><span class="sxs-lookup"><span data-stu-id="59da7-109">EXAMPLES</span></span>

### <span data-ttu-id="59da7-110">예제 1: 사용 중인 Kusto 데이터베이스 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="59da7-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="59da7-111">위의 명령은 "mykustodatabase"라는 Kusto 데이터베이스가 "testnewkustocluster" 클러스터에 있는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="59da7-112">예제 2: 사용되지 않는 Kusto 데이터베이스 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="59da7-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="59da7-113">위의 명령은 "mykustodatabase2"라는 Kusto 데이터베이스가 "testnewkustocluster" 클러스터에 있는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="59da7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="59da7-114">PARAMETERS</span></span>

### <span data-ttu-id="59da7-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="59da7-115">-ClusterName</span></span>
<span data-ttu-id="59da7-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59da7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59da7-117">-DefaultProfile</span></span>
<span data-ttu-id="59da7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59da7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59da7-119">-InputObject</span></span>
<span data-ttu-id="59da7-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="59da7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59da7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="59da7-121">-Name</span></span>
<span data-ttu-id="59da7-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59da7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59da7-123">-ResourceGroupName</span></span>
<span data-ttu-id="59da7-124">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59da7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59da7-125">-SubscriptionId</span></span>
<span data-ttu-id="59da7-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="59da7-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59da7-128">-Type</span><span class="sxs-lookup"><span data-stu-id="59da7-128">-Type</span></span>
<span data-ttu-id="59da7-129">리소스 유형(예: Microsoft.Kusto/Clusters/databases)입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59da7-130">-확인</span><span class="sxs-lookup"><span data-stu-id="59da7-130">-Confirm</span></span>
<span data-ttu-id="59da7-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59da7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59da7-132">-WhatIf</span></span>
<span data-ttu-id="59da7-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59da7-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59da7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59da7-135">CommonParameters</span></span>
<span data-ttu-id="59da7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59da7-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59da7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59da7-138">입력</span><span class="sxs-lookup"><span data-stu-id="59da7-138">INPUTS</span></span>

### <span data-ttu-id="59da7-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="59da7-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="59da7-140">출력</span><span class="sxs-lookup"><span data-stu-id="59da7-140">OUTPUTS</span></span>

### <span data-ttu-id="59da7-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="59da7-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="59da7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59da7-142">NOTES</span></span>

<span data-ttu-id="59da7-143">별칭</span><span class="sxs-lookup"><span data-stu-id="59da7-143">ALIASES</span></span>

<span data-ttu-id="59da7-144">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="59da7-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="59da7-145">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59da7-146">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="59da7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="59da7-147">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="59da7-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59da7-148">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="59da7-149">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="59da7-150">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="59da7-151">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="59da7-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="59da7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59da7-153">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="59da7-154">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="59da7-155">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="59da7-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="59da7-157">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="59da7-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="59da7-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59da7-158">RELATED LINKS</span></span>

