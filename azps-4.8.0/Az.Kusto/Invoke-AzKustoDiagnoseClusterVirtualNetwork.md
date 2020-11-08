---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213552"
---
# <span data-ttu-id="dfe4b-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dfe4b-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="dfe4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe4b-103">서비스가 종속 된 외부 리소스에 대 한 네트워크 연결 상태를 진단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="dfe4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfe4b-104">SYNTAX</span></span>

### <span data-ttu-id="dfe4b-105">진단 (기본값)</span><span class="sxs-lookup"><span data-stu-id="dfe4b-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dfe4b-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfe4b-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfe4b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dfe4b-107">DESCRIPTION</span></span>
<span data-ttu-id="dfe4b-108">서비스가 종속 된 외부 리소스에 대 한 네트워크 연결 상태를 진단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="dfe4b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dfe4b-109">EXAMPLES</span></span>

### <span data-ttu-id="dfe4b-110">예제 1: 외부 리소스에 대 한 네트워크 연결 진단 표시</span><span class="sxs-lookup"><span data-stu-id="dfe4b-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="dfe4b-111">위의 명령은 "testnewkustocluster" 클러스터가 종속 된 외부 리소스에 대 한 네트워크 연결 상태를 진단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="dfe4b-112">변수</span><span class="sxs-lookup"><span data-stu-id="dfe4b-112">PARAMETERS</span></span>

### <span data-ttu-id="dfe4b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfe4b-113">-AsJob</span></span>
<span data-ttu-id="dfe4b-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="dfe4b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dfe4b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfe4b-115">-ClusterName</span></span>
<span data-ttu-id="dfe4b-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe4b-117">-DefaultProfile</span></span>
<span data-ttu-id="dfe4b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfe4b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfe4b-119">-InputObject</span></span>
<span data-ttu-id="dfe4b-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe4b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dfe4b-121">-NoWait</span></span>
<span data-ttu-id="dfe4b-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="dfe4b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfe4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfe4b-124">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe4b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfe4b-125">-SubscriptionId</span></span>
<span data-ttu-id="dfe4b-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfe4b-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe4b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="dfe4b-128">-Confirm</span></span>
<span data-ttu-id="dfe4b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe4b-130">-WhatIf</span></span>
<span data-ttu-id="dfe4b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe4b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe4b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe4b-133">CommonParameters</span></span>
<span data-ttu-id="dfe4b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe4b-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe4b-136">입력</span><span class="sxs-lookup"><span data-stu-id="dfe4b-136">INPUTS</span></span>

### <span data-ttu-id="dfe4b-137">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="dfe4b-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dfe4b-138">출력</span><span class="sxs-lookup"><span data-stu-id="dfe4b-138">OUTPUTS</span></span>

### <span data-ttu-id="dfe4b-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfe4b-139">System.String</span></span>

## <span data-ttu-id="dfe4b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="dfe4b-140">NOTES</span></span>

<span data-ttu-id="dfe4b-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="dfe4b-141">ALIASES</span></span>

<span data-ttu-id="dfe4b-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="dfe4b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfe4b-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfe4b-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfe4b-145">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dfe4b-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfe4b-146">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dfe4b-147">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dfe4b-148">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dfe4b-149">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dfe4b-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="dfe4b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfe4b-151">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dfe4b-152">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dfe4b-153">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dfe4b-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dfe4b-155">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe4b-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dfe4b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfe4b-156">RELATED LINKS</span></span>

