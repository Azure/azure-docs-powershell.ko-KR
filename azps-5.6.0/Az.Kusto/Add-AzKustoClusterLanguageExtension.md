---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 0e1cfc142c4c98614519c26639144cc701d2118c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964592"
---
# <span data-ttu-id="f22ab-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="f22ab-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="f22ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f22ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f22ab-103">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f22ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="f22ab-104">SYNTAX</span></span>

### <span data-ttu-id="f22ab-105">AddExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="f22ab-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f22ab-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f22ab-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f22ab-107">설명</span><span class="sxs-lookup"><span data-stu-id="f22ab-107">DESCRIPTION</span></span>
<span data-ttu-id="f22ab-108">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f22ab-109">예제</span><span class="sxs-lookup"><span data-stu-id="f22ab-109">EXAMPLES</span></span>

### <span data-ttu-id="f22ab-110">예제 1: 언어 확장 목록 추가</span><span class="sxs-lookup"><span data-stu-id="f22ab-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="f22ab-111">위의 명령은 KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="f22ab-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f22ab-112">PARAMETERS</span></span>

### <span data-ttu-id="f22ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f22ab-113">-AsJob</span></span>
<span data-ttu-id="f22ab-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f22ab-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f22ab-115">-ClusterName</span></span>
<span data-ttu-id="f22ab-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22ab-117">-DefaultProfile</span></span>
<span data-ttu-id="f22ab-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f22ab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f22ab-119">-InputObject</span></span>
<span data-ttu-id="f22ab-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f22ab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f22ab-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f22ab-121">-NoWait</span></span>
<span data-ttu-id="f22ab-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="f22ab-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f22ab-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f22ab-123">-PassThru</span></span>
<span data-ttu-id="f22ab-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f22ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="f22ab-126">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ab-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f22ab-127">-SubscriptionId</span></span>
<span data-ttu-id="f22ab-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f22ab-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ab-130">-Value</span><span class="sxs-lookup"><span data-stu-id="f22ab-130">-Value</span></span>
<span data-ttu-id="f22ab-131">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-131">The list of language extensions.</span></span>
<span data-ttu-id="f22ab-132">생성을 위해 VALUE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f22ab-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ab-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f22ab-133">-Confirm</span></span>
<span data-ttu-id="f22ab-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f22ab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22ab-135">-WhatIf</span></span>
<span data-ttu-id="f22ab-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f22ab-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f22ab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22ab-138">CommonParameters</span></span>
<span data-ttu-id="f22ab-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22ab-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f22ab-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22ab-141">입력</span><span class="sxs-lookup"><span data-stu-id="f22ab-141">INPUTS</span></span>

### <span data-ttu-id="f22ab-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f22ab-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f22ab-143">출력</span><span class="sxs-lookup"><span data-stu-id="f22ab-143">OUTPUTS</span></span>

### <span data-ttu-id="f22ab-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f22ab-144">System.Boolean</span></span>

## <span data-ttu-id="f22ab-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f22ab-145">NOTES</span></span>

<span data-ttu-id="f22ab-146">별칭</span><span class="sxs-lookup"><span data-stu-id="f22ab-146">ALIASES</span></span>

<span data-ttu-id="f22ab-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f22ab-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f22ab-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f22ab-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f22ab-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f22ab-150">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f22ab-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f22ab-151">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f22ab-152">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f22ab-153">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f22ab-154">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f22ab-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f22ab-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f22ab-156">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f22ab-157">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f22ab-158">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f22ab-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f22ab-160">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f22ab-161">VALUE <ILanguageExtension[]>: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="f22ab-162">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f22ab-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="f22ab-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f22ab-163">RELATED LINKS</span></span>

