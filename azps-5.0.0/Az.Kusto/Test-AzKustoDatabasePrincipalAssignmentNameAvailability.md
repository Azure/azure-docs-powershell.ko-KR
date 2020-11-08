---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f61bbfc57017f16f9fee0c05f57aa51bd21d364d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217720"
---
# <span data-ttu-id="63f15-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="63f15-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="63f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f15-102">SYNOPSIS</span></span>
<span data-ttu-id="63f15-103">데이터베이스 보안 주체 할당이 유효 하며 아직 사용 중인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="63f15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63f15-104">SYNTAX</span></span>

### <span data-ttu-id="63f15-105">CheckExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="63f15-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="63f15-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="63f15-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63f15-107">설명은</span><span class="sxs-lookup"><span data-stu-id="63f15-107">DESCRIPTION</span></span>
<span data-ttu-id="63f15-108">데이터베이스 보안 주체 할당이 유효 하며 아직 사용 중인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="63f15-109">예제의</span><span class="sxs-lookup"><span data-stu-id="63f15-109">EXAMPLES</span></span>

### <span data-ttu-id="63f15-110">예제 1: 사용 중인 데이터베이스 위치 지정 배정 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="63f15-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="63f15-111">위의 명령은 "myprincipal" 이라는 PrincipalAssignment이 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 있는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="63f15-112">예제 2: 사용 하지 않는 데이터베이스 위치 지정 할당 이름 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="63f15-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="63f15-113">위의 명령은 "myprincipal" 이라는 PrincipalAssignment이 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 있는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="63f15-114">변수</span><span class="sxs-lookup"><span data-stu-id="63f15-114">PARAMETERS</span></span>

### <span data-ttu-id="63f15-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="63f15-115">-ClusterName</span></span>
<span data-ttu-id="63f15-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="63f15-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63f15-117">-DatabaseName</span></span>
<span data-ttu-id="63f15-118">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="63f15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f15-119">-DefaultProfile</span></span>
<span data-ttu-id="63f15-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f15-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63f15-121">-InputObject</span></span>
<span data-ttu-id="63f15-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="63f15-123">-이름</span><span class="sxs-lookup"><span data-stu-id="63f15-123">-Name</span></span>
<span data-ttu-id="63f15-124">Principal 배정 자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="63f15-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f15-125">-ResourceGroupName</span></span>
<span data-ttu-id="63f15-126">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="63f15-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63f15-127">-SubscriptionId</span></span>
<span data-ttu-id="63f15-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="63f15-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="63f15-130">-Type</span><span class="sxs-lookup"><span data-stu-id="63f15-130">-Type</span></span>
<span data-ttu-id="63f15-131">리소스 유형입니다 (Microsoft. Kusto/클러스터/-데이터베이스/principalAssignments).</span><span class="sxs-lookup"><span data-stu-id="63f15-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="63f15-132">-확인</span><span class="sxs-lookup"><span data-stu-id="63f15-132">-Confirm</span></span>
<span data-ttu-id="63f15-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f15-134">-WhatIf</span></span>
<span data-ttu-id="63f15-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f15-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f15-137">CommonParameters</span></span>
<span data-ttu-id="63f15-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f15-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63f15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f15-140">입력</span><span class="sxs-lookup"><span data-stu-id="63f15-140">INPUTS</span></span>

### <span data-ttu-id="63f15-141">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="63f15-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="63f15-142">출력</span><span class="sxs-lookup"><span data-stu-id="63f15-142">OUTPUTS</span></span>

### <span data-ttu-id="63f15-143">Microsoft. Api20200614. ICheckNameResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63f15-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="63f15-144">상속자</span><span class="sxs-lookup"><span data-stu-id="63f15-144">NOTES</span></span>

<span data-ttu-id="63f15-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="63f15-145">ALIASES</span></span>

<span data-ttu-id="63f15-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="63f15-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63f15-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63f15-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="63f15-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63f15-149">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="63f15-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="63f15-150">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="63f15-151">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="63f15-152">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="63f15-153">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="63f15-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="63f15-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63f15-155">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="63f15-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="63f15-156">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="63f15-157">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="63f15-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="63f15-159">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f15-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="63f15-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63f15-160">RELATED LINKS</span></span>

