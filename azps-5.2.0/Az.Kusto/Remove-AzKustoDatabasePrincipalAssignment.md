---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334118"
---
# <span data-ttu-id="1c854-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="1c854-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="1c854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c854-102">SYNOPSIS</span></span>
<span data-ttu-id="1c854-103">Kusto principalAssignment를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="1c854-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c854-104">SYNTAX</span></span>

### <span data-ttu-id="1c854-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c854-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c854-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c854-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c854-107">설명</span><span class="sxs-lookup"><span data-stu-id="1c854-107">DESCRIPTION</span></span>
<span data-ttu-id="1c854-108">Kusto principalAssignment를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="1c854-109">예제</span><span class="sxs-lookup"><span data-stu-id="1c854-109">EXAMPLES</span></span>

### <span data-ttu-id="1c854-110">예제 1: 이름에 따라 기존 Kusto 데이터베이스 PrincipalAssignment 삭제</span><span class="sxs-lookup"><span data-stu-id="1c854-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="1c854-111">위의 명령은 Kusto 데이터베이스 "mykustodatabase"에서 "kustoprincipal1"이라는 PrincipalAssignment를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="1c854-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c854-112">PARAMETERS</span></span>

### <span data-ttu-id="1c854-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c854-113">-AsJob</span></span>
<span data-ttu-id="1c854-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1c854-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1c854-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1c854-115">-ClusterName</span></span>
<span data-ttu-id="1c854-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1c854-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c854-117">-DatabaseName</span></span>
<span data-ttu-id="1c854-118">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1c854-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c854-119">-DefaultProfile</span></span>
<span data-ttu-id="1c854-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c854-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c854-121">-InputObject</span></span>
<span data-ttu-id="1c854-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1c854-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c854-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1c854-123">-NoWait</span></span>
<span data-ttu-id="1c854-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1c854-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c854-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c854-125">-PassThru</span></span>
<span data-ttu-id="1c854-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c854-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="1c854-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="1c854-128">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="1c854-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c854-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c854-130">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1c854-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c854-131">-SubscriptionId</span></span>
<span data-ttu-id="1c854-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1c854-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1c854-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c854-134">-Confirm</span></span>
<span data-ttu-id="1c854-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c854-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c854-136">-WhatIf</span></span>
<span data-ttu-id="1c854-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c854-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c854-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c854-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c854-139">CommonParameters</span></span>
<span data-ttu-id="1c854-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c854-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c854-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c854-142">입력</span><span class="sxs-lookup"><span data-stu-id="1c854-142">INPUTS</span></span>

### <span data-ttu-id="1c854-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1c854-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1c854-144">출력</span><span class="sxs-lookup"><span data-stu-id="1c854-144">OUTPUTS</span></span>

### <span data-ttu-id="1c854-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c854-145">System.Boolean</span></span>

## <span data-ttu-id="1c854-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c854-146">NOTES</span></span>

<span data-ttu-id="1c854-147">별칭</span><span class="sxs-lookup"><span data-stu-id="1c854-147">ALIASES</span></span>

<span data-ttu-id="1c854-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1c854-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c854-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c854-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c854-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c854-151">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c854-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c854-152">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1c854-153">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1c854-154">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1c854-155">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1c854-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1c854-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c854-157">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1c854-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1c854-159">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1c854-160">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1c854-161">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1c854-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1c854-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c854-162">RELATED LINKS</span></span>

