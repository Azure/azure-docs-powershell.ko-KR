---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386289"
---
# <span data-ttu-id="a5290-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5290-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="a5290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5290-102">SYNOPSIS</span></span>
<span data-ttu-id="a5290-103">지정한 이름으로 연결된 데이터베이스 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="a5290-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5290-104">SYNTAX</span></span>

### <span data-ttu-id="a5290-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5290-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a5290-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a5290-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5290-107">설명</span><span class="sxs-lookup"><span data-stu-id="a5290-107">DESCRIPTION</span></span>
<span data-ttu-id="a5290-108">지정한 이름으로 연결된 데이터베이스 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="a5290-109">예제</span><span class="sxs-lookup"><span data-stu-id="a5290-109">EXAMPLES</span></span>

### <span data-ttu-id="a5290-110">예제 1: 이름에 따라 기존 AttachedDatabaseConfiguration 삭제</span><span class="sxs-lookup"><span data-stu-id="a5290-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="a5290-111">위의 명령은 클러스터 "testnewkustoclusterf"에서 AttachedDatabaseConfiguration "myfollowerconfiguration"에 정의된 팔로워 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="a5290-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5290-112">PARAMETERS</span></span>

### <span data-ttu-id="a5290-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5290-113">-AsJob</span></span>
<span data-ttu-id="a5290-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5290-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a5290-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a5290-115">-ClusterName</span></span>
<span data-ttu-id="a5290-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5290-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5290-117">-DefaultProfile</span></span>
<span data-ttu-id="a5290-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5290-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5290-119">-InputObject</span></span>
<span data-ttu-id="a5290-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a5290-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5290-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a5290-121">-Name</span></span>
<span data-ttu-id="a5290-122">연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5290-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5290-123">-NoWait</span></span>
<span data-ttu-id="a5290-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="a5290-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5290-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5290-125">-PassThru</span></span>
<span data-ttu-id="a5290-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a5290-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5290-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5290-128">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5290-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5290-129">-SubscriptionId</span></span>
<span data-ttu-id="a5290-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5290-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5290-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5290-132">-Confirm</span></span>
<span data-ttu-id="a5290-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5290-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5290-134">-WhatIf</span></span>
<span data-ttu-id="a5290-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5290-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5290-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5290-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5290-137">CommonParameters</span></span>
<span data-ttu-id="a5290-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5290-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5290-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5290-140">입력</span><span class="sxs-lookup"><span data-stu-id="a5290-140">INPUTS</span></span>

### <span data-ttu-id="a5290-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a5290-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a5290-142">출력</span><span class="sxs-lookup"><span data-stu-id="a5290-142">OUTPUTS</span></span>

### <span data-ttu-id="a5290-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5290-143">System.Boolean</span></span>

## <span data-ttu-id="a5290-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5290-144">NOTES</span></span>

<span data-ttu-id="a5290-145">별칭</span><span class="sxs-lookup"><span data-stu-id="a5290-145">ALIASES</span></span>

<span data-ttu-id="a5290-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5290-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5290-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5290-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5290-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5290-149">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5290-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5290-150">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a5290-151">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a5290-152">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a5290-153">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a5290-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a5290-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5290-155">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a5290-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a5290-157">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a5290-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a5290-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5290-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a5290-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5290-160">RELATED LINKS</span></span>

