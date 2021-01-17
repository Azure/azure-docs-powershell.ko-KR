---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350925"
---
# <span data-ttu-id="a5e65-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a5e65-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="a5e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e65-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e65-103">클러스터 이름이 유효하고 아직 사용 중이지 않은지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="a5e65-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5e65-104">SYNTAX</span></span>

### <span data-ttu-id="a5e65-105">CheckExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5e65-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5e65-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a5e65-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5e65-107">설명</span><span class="sxs-lookup"><span data-stu-id="a5e65-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e65-108">클러스터 이름이 유효하고 아직 사용 중이지 않은지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="a5e65-109">예제</span><span class="sxs-lookup"><span data-stu-id="a5e65-109">EXAMPLES</span></span>

### <span data-ttu-id="a5e65-110">예제 1: 사용 중인 Kusto 클러스터 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="a5e65-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="a5e65-111">위의 명령은 "testnewkustocluster"라는 Kusto 클러스터가 "미국 동부" 지역에 있는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="a5e65-112">예제 2: 사용되지 않는 Kusto 클러스터 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="a5e65-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="a5e65-113">위의 명령은 "availablekustocluster"라는 Kusto 클러스터가 "미국 동부" 지역에 있는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="a5e65-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5e65-114">PARAMETERS</span></span>

### <span data-ttu-id="a5e65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e65-115">-DefaultProfile</span></span>
<span data-ttu-id="a5e65-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e65-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e65-117">-InputObject</span></span>
<span data-ttu-id="a5e65-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a5e65-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5e65-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a5e65-119">-Location</span></span>
<span data-ttu-id="a5e65-120">Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-120">Azure location.</span></span>

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

### <span data-ttu-id="a5e65-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a5e65-121">-Name</span></span>
<span data-ttu-id="a5e65-122">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-122">Cluster name.</span></span>

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

### <span data-ttu-id="a5e65-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5e65-123">-SubscriptionId</span></span>
<span data-ttu-id="a5e65-124">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5e65-125">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5e65-126">-Type</span><span class="sxs-lookup"><span data-stu-id="a5e65-126">-Type</span></span>
<span data-ttu-id="a5e65-127">리소스 유형, Microsoft.Kusto/clusters입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="a5e65-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5e65-128">-Confirm</span></span>
<span data-ttu-id="a5e65-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e65-130">-WhatIf</span></span>
<span data-ttu-id="a5e65-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5e65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e65-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e65-133">CommonParameters</span></span>
<span data-ttu-id="a5e65-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e65-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5e65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e65-136">입력</span><span class="sxs-lookup"><span data-stu-id="a5e65-136">INPUTS</span></span>

### <span data-ttu-id="a5e65-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a5e65-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a5e65-138">출력</span><span class="sxs-lookup"><span data-stu-id="a5e65-138">OUTPUTS</span></span>

### <span data-ttu-id="a5e65-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="a5e65-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="a5e65-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5e65-140">NOTES</span></span>

<span data-ttu-id="a5e65-141">별칭</span><span class="sxs-lookup"><span data-stu-id="a5e65-141">ALIASES</span></span>

<span data-ttu-id="a5e65-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5e65-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5e65-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5e65-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5e65-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5e65-145">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5e65-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5e65-146">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a5e65-147">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a5e65-148">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a5e65-149">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a5e65-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a5e65-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5e65-151">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a5e65-152">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a5e65-153">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a5e65-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a5e65-155">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e65-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a5e65-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5e65-156">RELATED LINKS</span></span>

