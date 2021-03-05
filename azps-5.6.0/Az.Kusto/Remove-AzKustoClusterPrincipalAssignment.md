---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b2dd7c125fbf2529e7dc214efdc9ef5fdef1ace0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001259"
---
# <span data-ttu-id="b7160-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b7160-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="b7160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7160-102">SYNOPSIS</span></span>
<span data-ttu-id="b7160-103">Kusto 클러스터 보안 주체Assignment를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b7160-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7160-104">SYNTAX</span></span>

### <span data-ttu-id="b7160-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7160-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7160-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7160-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7160-107">설명</span><span class="sxs-lookup"><span data-stu-id="b7160-107">DESCRIPTION</span></span>
<span data-ttu-id="b7160-108">Kusto 클러스터 보안 주체Assignment를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b7160-109">예제</span><span class="sxs-lookup"><span data-stu-id="b7160-109">EXAMPLES</span></span>

### <span data-ttu-id="b7160-110">예제 1: 이름에 의해 기존 Kusto 클러스터 PrincipalAssignment 삭제</span><span class="sxs-lookup"><span data-stu-id="b7160-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="b7160-111">위의 명령은 Kusto 클러스터 "testnewkustocluster"에서 "kustoprincipal1"이라는 PrincipalAssignment를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="b7160-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7160-112">PARAMETERS</span></span>

### <span data-ttu-id="b7160-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7160-113">-AsJob</span></span>
<span data-ttu-id="b7160-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b7160-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7160-115">-ClusterName</span></span>
<span data-ttu-id="b7160-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b7160-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7160-117">-DefaultProfile</span></span>
<span data-ttu-id="b7160-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7160-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7160-119">-InputObject</span></span>
<span data-ttu-id="b7160-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b7160-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7160-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b7160-121">-NoWait</span></span>
<span data-ttu-id="b7160-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="b7160-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b7160-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7160-123">-PassThru</span></span>
<span data-ttu-id="b7160-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b7160-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b7160-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="b7160-126">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="b7160-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7160-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7160-128">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b7160-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7160-129">-SubscriptionId</span></span>
<span data-ttu-id="b7160-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7160-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7160-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b7160-132">-Confirm</span></span>
<span data-ttu-id="b7160-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7160-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7160-134">-WhatIf</span></span>
<span data-ttu-id="b7160-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7160-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7160-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7160-137">CommonParameters</span></span>
<span data-ttu-id="b7160-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7160-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7160-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7160-140">입력</span><span class="sxs-lookup"><span data-stu-id="b7160-140">INPUTS</span></span>

### <span data-ttu-id="b7160-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b7160-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b7160-142">출력</span><span class="sxs-lookup"><span data-stu-id="b7160-142">OUTPUTS</span></span>

### <span data-ttu-id="b7160-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7160-143">System.Boolean</span></span>

## <span data-ttu-id="b7160-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7160-144">NOTES</span></span>

<span data-ttu-id="b7160-145">별칭</span><span class="sxs-lookup"><span data-stu-id="b7160-145">ALIASES</span></span>

<span data-ttu-id="b7160-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b7160-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7160-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7160-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7160-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7160-149">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7160-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7160-150">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b7160-151">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b7160-152">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b7160-153">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b7160-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b7160-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7160-155">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b7160-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b7160-157">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b7160-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b7160-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b7160-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b7160-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7160-160">RELATED LINKS</span></span>

