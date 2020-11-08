---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049037"
---
# <span data-ttu-id="99279-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="99279-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="99279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99279-102">SYNOPSIS</span></span>
<span data-ttu-id="99279-103">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="99279-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99279-104">SYNTAX</span></span>

### <span data-ttu-id="99279-105">RemoveExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="99279-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99279-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="99279-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99279-107">설명은</span><span class="sxs-lookup"><span data-stu-id="99279-107">DESCRIPTION</span></span>
<span data-ttu-id="99279-108">KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="99279-109">예제의</span><span class="sxs-lookup"><span data-stu-id="99279-109">EXAMPLES</span></span>

### <span data-ttu-id="99279-110">예제 1: 클러스터에서 언어 확장 목록 제거</span><span class="sxs-lookup"><span data-stu-id="99279-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="99279-111">위 명령은 KQL 쿼리 내에서 실행할 수 있는 언어 확장 목록을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="99279-112">변수</span><span class="sxs-lookup"><span data-stu-id="99279-112">PARAMETERS</span></span>

### <span data-ttu-id="99279-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99279-113">-AsJob</span></span>
<span data-ttu-id="99279-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="99279-114">Run the command as a job</span></span>

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

### <span data-ttu-id="99279-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99279-115">-ClusterName</span></span>
<span data-ttu-id="99279-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="99279-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99279-117">-DefaultProfile</span></span>
<span data-ttu-id="99279-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99279-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99279-119">-InputObject</span></span>
<span data-ttu-id="99279-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99279-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99279-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="99279-121">-NoWait</span></span>
<span data-ttu-id="99279-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="99279-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99279-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99279-123">-PassThru</span></span>
<span data-ttu-id="99279-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="99279-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99279-125">-ResourceGroupName</span></span>
<span data-ttu-id="99279-126">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="99279-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99279-127">-SubscriptionId</span></span>
<span data-ttu-id="99279-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99279-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99279-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99279-130">-값</span><span class="sxs-lookup"><span data-stu-id="99279-130">-Value</span></span>
<span data-ttu-id="99279-131">언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-131">The list of language extensions.</span></span>
<span data-ttu-id="99279-132">생성 하려면 값 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99279-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="99279-133">-확인</span><span class="sxs-lookup"><span data-stu-id="99279-133">-Confirm</span></span>
<span data-ttu-id="99279-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99279-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99279-135">-WhatIf</span></span>
<span data-ttu-id="99279-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99279-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99279-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99279-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99279-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99279-138">CommonParameters</span></span>
<span data-ttu-id="99279-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99279-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99279-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99279-141">입력</span><span class="sxs-lookup"><span data-stu-id="99279-141">INPUTS</span></span>

### <span data-ttu-id="99279-142">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="99279-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="99279-143">출력</span><span class="sxs-lookup"><span data-stu-id="99279-143">OUTPUTS</span></span>

### <span data-ttu-id="99279-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="99279-144">System.Boolean</span></span>

## <span data-ttu-id="99279-145">상속자</span><span class="sxs-lookup"><span data-stu-id="99279-145">NOTES</span></span>

<span data-ttu-id="99279-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="99279-146">ALIASES</span></span>

<span data-ttu-id="99279-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="99279-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99279-148">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99279-149">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="99279-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99279-150">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="99279-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99279-151">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="99279-152">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="99279-153">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="99279-154">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="99279-155">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="99279-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99279-156">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="99279-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="99279-157">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="99279-158">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="99279-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99279-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="99279-160">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="99279-161">값 <ILanguageExtension [] >: 언어 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="99279-162">`[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99279-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="99279-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99279-163">RELATED LINKS</span></span>

