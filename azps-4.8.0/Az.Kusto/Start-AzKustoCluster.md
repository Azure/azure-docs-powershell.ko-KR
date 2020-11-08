---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048210"
---
# <span data-ttu-id="bddc9-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="bddc9-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="bddc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bddc9-102">SYNOPSIS</span></span>
<span data-ttu-id="bddc9-103">클러스터에 대 한 Kusto 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="bddc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bddc9-104">SYNTAX</span></span>

### <span data-ttu-id="bddc9-105">시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bddc9-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bddc9-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bddc9-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bddc9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bddc9-107">DESCRIPTION</span></span>
<span data-ttu-id="bddc9-108">클러스터에 대 한 Kusto 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="bddc9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bddc9-109">EXAMPLES</span></span>

### <span data-ttu-id="bddc9-110">예제 1: 클러스터에 대 한 Kusto</span><span class="sxs-lookup"><span data-stu-id="bddc9-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="bddc9-111">위의 명령은 Kusto를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="bddc9-112">변수</span><span class="sxs-lookup"><span data-stu-id="bddc9-112">PARAMETERS</span></span>

### <span data-ttu-id="bddc9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bddc9-113">-AsJob</span></span>
<span data-ttu-id="bddc9-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bddc9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bddc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bddc9-115">-DefaultProfile</span></span>
<span data-ttu-id="bddc9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bddc9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bddc9-117">-InputObject</span></span>
<span data-ttu-id="bddc9-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bddc9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="bddc9-119">-Name</span></span>
<span data-ttu-id="bddc9-120">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddc9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bddc9-121">-NoWait</span></span>
<span data-ttu-id="bddc9-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bddc9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bddc9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bddc9-123">-PassThru</span></span>
<span data-ttu-id="bddc9-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bddc9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bddc9-125">-ResourceGroupName</span></span>
<span data-ttu-id="bddc9-126">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddc9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bddc9-127">-SubscriptionId</span></span>
<span data-ttu-id="bddc9-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bddc9-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddc9-130">-확인</span><span class="sxs-lookup"><span data-stu-id="bddc9-130">-Confirm</span></span>
<span data-ttu-id="bddc9-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bddc9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bddc9-132">-WhatIf</span></span>
<span data-ttu-id="bddc9-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bddc9-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bddc9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bddc9-135">CommonParameters</span></span>
<span data-ttu-id="bddc9-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bddc9-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bddc9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bddc9-138">입력</span><span class="sxs-lookup"><span data-stu-id="bddc9-138">INPUTS</span></span>

### <span data-ttu-id="bddc9-139">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="bddc9-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bddc9-140">출력</span><span class="sxs-lookup"><span data-stu-id="bddc9-140">OUTPUTS</span></span>

### <span data-ttu-id="bddc9-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bddc9-141">System.Boolean</span></span>

## <span data-ttu-id="bddc9-142">상속자</span><span class="sxs-lookup"><span data-stu-id="bddc9-142">NOTES</span></span>

<span data-ttu-id="bddc9-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="bddc9-143">ALIASES</span></span>

<span data-ttu-id="bddc9-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bddc9-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bddc9-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bddc9-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="bddc9-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bddc9-147">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bddc9-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bddc9-148">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bddc9-149">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bddc9-150">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bddc9-151">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bddc9-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="bddc9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bddc9-153">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="bddc9-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bddc9-154">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bddc9-155">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bddc9-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bddc9-157">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bddc9-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bddc9-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bddc9-158">RELATED LINKS</span></span>

