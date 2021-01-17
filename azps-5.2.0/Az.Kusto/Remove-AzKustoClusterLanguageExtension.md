---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362230"
---
# <span data-ttu-id="efc91-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="efc91-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="efc91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc91-102">SYNOPSIS</span></span>
<span data-ttu-id="efc91-103">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="efc91-104">구문</span><span class="sxs-lookup"><span data-stu-id="efc91-104">SYNTAX</span></span>

### <span data-ttu-id="efc91-105">RemoveExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="efc91-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efc91-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efc91-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efc91-107">설명</span><span class="sxs-lookup"><span data-stu-id="efc91-107">DESCRIPTION</span></span>
<span data-ttu-id="efc91-108">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="efc91-109">예제</span><span class="sxs-lookup"><span data-stu-id="efc91-109">EXAMPLES</span></span>

### <span data-ttu-id="efc91-110">예제 1: 클러스터에서 언어 확장 목록 제거</span><span class="sxs-lookup"><span data-stu-id="efc91-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="efc91-111">위의 명령은 KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="efc91-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efc91-112">PARAMETERS</span></span>

### <span data-ttu-id="efc91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efc91-113">-AsJob</span></span>
<span data-ttu-id="efc91-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="efc91-114">Run the command as a job</span></span>

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

### <span data-ttu-id="efc91-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="efc91-115">-ClusterName</span></span>
<span data-ttu-id="efc91-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="efc91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc91-117">-DefaultProfile</span></span>
<span data-ttu-id="efc91-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efc91-119">-InputObject</span></span>
<span data-ttu-id="efc91-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="efc91-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="efc91-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="efc91-121">-NoWait</span></span>
<span data-ttu-id="efc91-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="efc91-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="efc91-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efc91-123">-PassThru</span></span>
<span data-ttu-id="efc91-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="efc91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc91-125">-ResourceGroupName</span></span>
<span data-ttu-id="efc91-126">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="efc91-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efc91-127">-SubscriptionId</span></span>
<span data-ttu-id="efc91-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="efc91-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="efc91-130">-Value</span><span class="sxs-lookup"><span data-stu-id="efc91-130">-Value</span></span>
<span data-ttu-id="efc91-131">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-131">The list of language extensions.</span></span>
<span data-ttu-id="efc91-132">생성을 위해 VALUE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="efc91-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc91-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efc91-133">-Confirm</span></span>
<span data-ttu-id="efc91-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc91-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc91-135">-WhatIf</span></span>
<span data-ttu-id="efc91-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="efc91-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc91-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc91-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc91-138">CommonParameters</span></span>
<span data-ttu-id="efc91-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc91-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="efc91-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc91-141">입력</span><span class="sxs-lookup"><span data-stu-id="efc91-141">INPUTS</span></span>

### <span data-ttu-id="efc91-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="efc91-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="efc91-143">출력</span><span class="sxs-lookup"><span data-stu-id="efc91-143">OUTPUTS</span></span>

### <span data-ttu-id="efc91-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efc91-144">System.Boolean</span></span>

## <span data-ttu-id="efc91-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efc91-145">NOTES</span></span>

<span data-ttu-id="efc91-146">별칭</span><span class="sxs-lookup"><span data-stu-id="efc91-146">ALIASES</span></span>

<span data-ttu-id="efc91-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="efc91-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efc91-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efc91-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efc91-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efc91-150">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efc91-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efc91-151">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="efc91-152">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="efc91-153">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="efc91-154">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="efc91-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="efc91-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efc91-156">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="efc91-157">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="efc91-158">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="efc91-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="efc91-160">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="efc91-161">VALUE <ILanguageExtension[]>: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="efc91-162">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efc91-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="efc91-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efc91-163">RELATED LINKS</span></span>
