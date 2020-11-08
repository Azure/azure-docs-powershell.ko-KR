---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048207"
---
# <span data-ttu-id="53f18-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="53f18-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="53f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f18-102">SYNOPSIS</span></span>
<span data-ttu-id="53f18-103">Kusto를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="53f18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53f18-104">SYNTAX</span></span>

### <span data-ttu-id="53f18-105">중지 (기본값)</span><span class="sxs-lookup"><span data-stu-id="53f18-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53f18-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="53f18-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53f18-107">설명은</span><span class="sxs-lookup"><span data-stu-id="53f18-107">DESCRIPTION</span></span>
<span data-ttu-id="53f18-108">Kusto를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="53f18-109">예제의</span><span class="sxs-lookup"><span data-stu-id="53f18-109">EXAMPLES</span></span>

### <span data-ttu-id="53f18-110">예제 1: 클러스터에 대 한 Kusto</span><span class="sxs-lookup"><span data-stu-id="53f18-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="53f18-111">위 명령으로 Kusto를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="53f18-112">변수</span><span class="sxs-lookup"><span data-stu-id="53f18-112">PARAMETERS</span></span>

### <span data-ttu-id="53f18-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53f18-113">-AsJob</span></span>
<span data-ttu-id="53f18-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="53f18-114">Run the command as a job</span></span>

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

### <span data-ttu-id="53f18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f18-115">-DefaultProfile</span></span>
<span data-ttu-id="53f18-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f18-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53f18-117">-InputObject</span></span>
<span data-ttu-id="53f18-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53f18-119">-이름</span><span class="sxs-lookup"><span data-stu-id="53f18-119">-Name</span></span>
<span data-ttu-id="53f18-120">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f18-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="53f18-121">-NoWait</span></span>
<span data-ttu-id="53f18-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="53f18-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="53f18-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53f18-123">-PassThru</span></span>
<span data-ttu-id="53f18-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="53f18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f18-125">-ResourceGroupName</span></span>
<span data-ttu-id="53f18-126">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f18-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53f18-127">-SubscriptionId</span></span>
<span data-ttu-id="53f18-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="53f18-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f18-130">-확인</span><span class="sxs-lookup"><span data-stu-id="53f18-130">-Confirm</span></span>
<span data-ttu-id="53f18-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f18-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f18-132">-WhatIf</span></span>
<span data-ttu-id="53f18-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f18-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f18-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f18-135">CommonParameters</span></span>
<span data-ttu-id="53f18-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f18-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53f18-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f18-138">입력</span><span class="sxs-lookup"><span data-stu-id="53f18-138">INPUTS</span></span>

### <span data-ttu-id="53f18-139">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="53f18-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="53f18-140">출력</span><span class="sxs-lookup"><span data-stu-id="53f18-140">OUTPUTS</span></span>

### <span data-ttu-id="53f18-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="53f18-141">System.Boolean</span></span>

## <span data-ttu-id="53f18-142">상속자</span><span class="sxs-lookup"><span data-stu-id="53f18-142">NOTES</span></span>

<span data-ttu-id="53f18-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="53f18-143">ALIASES</span></span>

<span data-ttu-id="53f18-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="53f18-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53f18-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53f18-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="53f18-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53f18-147">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="53f18-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53f18-148">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="53f18-149">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="53f18-150">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="53f18-151">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="53f18-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="53f18-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53f18-153">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="53f18-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="53f18-154">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="53f18-155">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="53f18-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="53f18-157">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f18-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="53f18-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53f18-158">RELATED LINKS</span></span>

