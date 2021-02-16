---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194284"
---
# <span data-ttu-id="163ba-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="163ba-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="163ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="163ba-102">SYNOPSIS</span></span>
<span data-ttu-id="163ba-103">지정한 이름의 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="163ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="163ba-104">SYNTAX</span></span>

### <span data-ttu-id="163ba-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="163ba-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="163ba-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="163ba-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="163ba-107">설명</span><span class="sxs-lookup"><span data-stu-id="163ba-107">DESCRIPTION</span></span>
<span data-ttu-id="163ba-108">지정한 이름의 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="163ba-109">예제</span><span class="sxs-lookup"><span data-stu-id="163ba-109">EXAMPLES</span></span>

### <span data-ttu-id="163ba-110">예제 1: 이름으로 기존 Kusto 데이터베이스 삭제</span><span class="sxs-lookup"><span data-stu-id="163ba-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="163ba-111">위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"에서 "mykustodatabase"라는 Kusto 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="163ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="163ba-112">PARAMETERS</span></span>

### <span data-ttu-id="163ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="163ba-113">-AsJob</span></span>
<span data-ttu-id="163ba-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="163ba-114">Run the command as a job</span></span>

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

### <span data-ttu-id="163ba-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="163ba-115">-ClusterName</span></span>
<span data-ttu-id="163ba-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="163ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163ba-117">-DefaultProfile</span></span>
<span data-ttu-id="163ba-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="163ba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="163ba-119">-InputObject</span></span>
<span data-ttu-id="163ba-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="163ba-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="163ba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="163ba-121">-Name</span></span>
<span data-ttu-id="163ba-122">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163ba-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="163ba-123">-NoWait</span></span>
<span data-ttu-id="163ba-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="163ba-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="163ba-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="163ba-125">-PassThru</span></span>
<span data-ttu-id="163ba-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="163ba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163ba-127">-ResourceGroupName</span></span>
<span data-ttu-id="163ba-128">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="163ba-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="163ba-129">-SubscriptionId</span></span>
<span data-ttu-id="163ba-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="163ba-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="163ba-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="163ba-132">-Confirm</span></span>
<span data-ttu-id="163ba-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="163ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="163ba-134">-WhatIf</span></span>
<span data-ttu-id="163ba-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="163ba-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="163ba-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="163ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163ba-137">CommonParameters</span></span>
<span data-ttu-id="163ba-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163ba-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="163ba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163ba-140">입력</span><span class="sxs-lookup"><span data-stu-id="163ba-140">INPUTS</span></span>

### <span data-ttu-id="163ba-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="163ba-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="163ba-142">출력</span><span class="sxs-lookup"><span data-stu-id="163ba-142">OUTPUTS</span></span>

### <span data-ttu-id="163ba-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="163ba-143">System.Boolean</span></span>

## <span data-ttu-id="163ba-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="163ba-144">NOTES</span></span>

<span data-ttu-id="163ba-145">별칭</span><span class="sxs-lookup"><span data-stu-id="163ba-145">ALIASES</span></span>

<span data-ttu-id="163ba-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="163ba-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="163ba-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="163ba-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="163ba-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="163ba-149">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="163ba-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="163ba-150">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="163ba-151">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="163ba-152">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="163ba-153">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="163ba-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="163ba-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="163ba-155">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="163ba-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="163ba-157">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="163ba-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="163ba-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="163ba-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="163ba-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="163ba-160">RELATED LINKS</span></span>

