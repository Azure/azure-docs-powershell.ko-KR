---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 14eee624f4de3129ddeefee05d402abb0cb686db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180425"
---
# <span data-ttu-id="5cd06-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5cd06-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="5cd06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd06-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd06-103">데이터 연결 이름이 유효하고 아직 사용 중이지 않은지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="5cd06-104">구문</span><span class="sxs-lookup"><span data-stu-id="5cd06-104">SYNTAX</span></span>

### <span data-ttu-id="5cd06-105">CheckExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5cd06-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5cd06-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5cd06-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cd06-107">설명</span><span class="sxs-lookup"><span data-stu-id="5cd06-107">DESCRIPTION</span></span>
<span data-ttu-id="5cd06-108">데이터 연결 이름이 유효하고 아직 사용 중이지 않은지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="5cd06-109">예제</span><span class="sxs-lookup"><span data-stu-id="5cd06-109">EXAMPLES</span></span>

### <span data-ttu-id="5cd06-110">예제 1: 사용 중 데이터 연결 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="5cd06-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="5cd06-111">위의 명령은 "mykustodataconnection"이라는 데이터 연결이 "mykustodatabase" 데이터베이스에 있는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="5cd06-112">예제 2: 사용되지 않는 데이터 연결 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="5cd06-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="5cd06-113">위의 명령은 "mydataconnection"이라는 데이터 연결이 "mykustodatabase" 데이터베이스에 있는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="5cd06-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd06-114">PARAMETERS</span></span>

### <span data-ttu-id="5cd06-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5cd06-115">-ClusterName</span></span>
<span data-ttu-id="5cd06-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5cd06-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5cd06-117">-DatabaseName</span></span>
<span data-ttu-id="5cd06-118">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5cd06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd06-119">-DefaultProfile</span></span>
<span data-ttu-id="5cd06-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cd06-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cd06-121">-InputObject</span></span>
<span data-ttu-id="5cd06-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5cd06-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cd06-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5cd06-123">-Name</span></span>
<span data-ttu-id="5cd06-124">데이터 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-124">Data Connection name.</span></span>

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

### <span data-ttu-id="5cd06-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd06-125">-ResourceGroupName</span></span>
<span data-ttu-id="5cd06-126">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5cd06-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cd06-127">-SubscriptionId</span></span>
<span data-ttu-id="5cd06-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5cd06-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5cd06-130">-Type</span><span class="sxs-lookup"><span data-stu-id="5cd06-130">-Type</span></span>
<span data-ttu-id="5cd06-131">리소스 유형, Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="5cd06-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="5cd06-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cd06-132">-Confirm</span></span>
<span data-ttu-id="5cd06-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd06-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd06-134">-WhatIf</span></span>
<span data-ttu-id="5cd06-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5cd06-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd06-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd06-137">CommonParameters</span></span>
<span data-ttu-id="5cd06-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd06-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5cd06-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd06-140">입력</span><span class="sxs-lookup"><span data-stu-id="5cd06-140">INPUTS</span></span>

### <span data-ttu-id="5cd06-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5cd06-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5cd06-142">출력</span><span class="sxs-lookup"><span data-stu-id="5cd06-142">OUTPUTS</span></span>

### <span data-ttu-id="5cd06-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="5cd06-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="5cd06-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5cd06-144">NOTES</span></span>

<span data-ttu-id="5cd06-145">별칭</span><span class="sxs-lookup"><span data-stu-id="5cd06-145">ALIASES</span></span>

<span data-ttu-id="5cd06-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5cd06-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cd06-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cd06-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cd06-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cd06-149">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5cd06-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cd06-150">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5cd06-151">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5cd06-152">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5cd06-153">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5cd06-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5cd06-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cd06-155">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5cd06-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5cd06-157">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5cd06-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5cd06-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5cd06-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5cd06-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cd06-160">RELATED LINKS</span></span>

