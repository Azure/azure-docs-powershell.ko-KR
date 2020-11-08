---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211851"
---
# <span data-ttu-id="09bf4-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="09bf4-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="09bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="09bf4-103">클러스터 이름이 유효 하며 아직 사용 중이 아닌지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="09bf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09bf4-104">SYNTAX</span></span>

### <span data-ttu-id="09bf4-105">CheckExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="09bf4-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09bf4-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09bf4-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09bf4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="09bf4-107">DESCRIPTION</span></span>
<span data-ttu-id="09bf4-108">클러스터 이름이 유효 하며 아직 사용 중이 아닌지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="09bf4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="09bf4-109">EXAMPLES</span></span>

### <span data-ttu-id="09bf4-110">예제 1: 사용 중인 클러스터 이름에 대 한 Kusto의 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="09bf4-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="09bf4-111">위 명령에 "testnewkustocluster" 이라는 클러스터의 Kusto가 "동부 US" 지역에 존재 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="09bf4-112">예제 2: 사용 하지 않는 클러스터 이름에 대 한 Kusto의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="09bf4-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="09bf4-113">위 명령에 "availablekustocluster" 이라는 클러스터의 Kusto가 "동부 US" 지역에 존재 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="09bf4-114">변수</span><span class="sxs-lookup"><span data-stu-id="09bf4-114">PARAMETERS</span></span>

### <span data-ttu-id="09bf4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bf4-115">-DefaultProfile</span></span>
<span data-ttu-id="09bf4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09bf4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09bf4-117">-InputObject</span></span>
<span data-ttu-id="09bf4-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09bf4-119">-위치</span><span class="sxs-lookup"><span data-stu-id="09bf4-119">-Location</span></span>
<span data-ttu-id="09bf4-120">Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="09bf4-120">Azure location.</span></span>

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

### <span data-ttu-id="09bf4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="09bf4-121">-Name</span></span>
<span data-ttu-id="09bf4-122">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-122">Cluster name.</span></span>

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

### <span data-ttu-id="09bf4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09bf4-123">-SubscriptionId</span></span>
<span data-ttu-id="09bf4-124">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="09bf4-125">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09bf4-126">-Type</span><span class="sxs-lookup"><span data-stu-id="09bf4-126">-Type</span></span>
<span data-ttu-id="09bf4-127">리소스 유형으로, Microsoft Kusto/클러스터.</span><span class="sxs-lookup"><span data-stu-id="09bf4-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="09bf4-128">-확인</span><span class="sxs-lookup"><span data-stu-id="09bf4-128">-Confirm</span></span>
<span data-ttu-id="09bf4-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09bf4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09bf4-130">-WhatIf</span></span>
<span data-ttu-id="09bf4-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09bf4-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09bf4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bf4-133">CommonParameters</span></span>
<span data-ttu-id="09bf4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bf4-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09bf4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bf4-136">입력</span><span class="sxs-lookup"><span data-stu-id="09bf4-136">INPUTS</span></span>

### <span data-ttu-id="09bf4-137">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="09bf4-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="09bf4-138">출력</span><span class="sxs-lookup"><span data-stu-id="09bf4-138">OUTPUTS</span></span>

### <span data-ttu-id="09bf4-139">Microsoft. Api20200614. ICheckNameResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="09bf4-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="09bf4-140">상속자</span><span class="sxs-lookup"><span data-stu-id="09bf4-140">NOTES</span></span>

<span data-ttu-id="09bf4-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="09bf4-141">ALIASES</span></span>

<span data-ttu-id="09bf4-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="09bf4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09bf4-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09bf4-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="09bf4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09bf4-145">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="09bf4-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09bf4-146">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="09bf4-147">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="09bf4-148">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="09bf4-149">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="09bf4-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="09bf4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09bf4-151">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="09bf4-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="09bf4-152">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="09bf4-153">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="09bf4-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="09bf4-155">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf4-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="09bf4-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09bf4-156">RELATED LINKS</span></span>

