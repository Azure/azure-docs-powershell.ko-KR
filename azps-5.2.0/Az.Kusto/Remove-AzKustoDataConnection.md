---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369370"
---
# <span data-ttu-id="1fcac-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1fcac-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="1fcac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fcac-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcac-103">지정한 이름의 데이터 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="1fcac-104">구문</span><span class="sxs-lookup"><span data-stu-id="1fcac-104">SYNTAX</span></span>

### <span data-ttu-id="1fcac-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="1fcac-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1fcac-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1fcac-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fcac-107">설명</span><span class="sxs-lookup"><span data-stu-id="1fcac-107">DESCRIPTION</span></span>
<span data-ttu-id="1fcac-108">지정한 이름의 데이터 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="1fcac-109">예제</span><span class="sxs-lookup"><span data-stu-id="1fcac-109">EXAMPLES</span></span>

### <span data-ttu-id="1fcac-110">예제 1: 이름에 따라 기존 데이터 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="1fcac-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="1fcac-111">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에서 "mykustodataconnection"이라는 데이터 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="1fcac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fcac-112">PARAMETERS</span></span>

### <span data-ttu-id="1fcac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fcac-113">-AsJob</span></span>
<span data-ttu-id="1fcac-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1fcac-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1fcac-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1fcac-115">-ClusterName</span></span>
<span data-ttu-id="1fcac-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1fcac-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fcac-117">-DatabaseName</span></span>
<span data-ttu-id="1fcac-118">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1fcac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcac-119">-DefaultProfile</span></span>
<span data-ttu-id="1fcac-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fcac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fcac-121">-InputObject</span></span>
<span data-ttu-id="1fcac-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1fcac-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1fcac-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1fcac-123">-Name</span></span>
<span data-ttu-id="1fcac-124">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcac-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1fcac-125">-NoWait</span></span>
<span data-ttu-id="1fcac-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1fcac-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1fcac-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fcac-127">-PassThru</span></span>
<span data-ttu-id="1fcac-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1fcac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcac-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fcac-130">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1fcac-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fcac-131">-SubscriptionId</span></span>
<span data-ttu-id="1fcac-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fcac-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1fcac-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fcac-134">-Confirm</span></span>
<span data-ttu-id="1fcac-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcac-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcac-136">-WhatIf</span></span>
<span data-ttu-id="1fcac-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1fcac-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcac-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcac-139">CommonParameters</span></span>
<span data-ttu-id="1fcac-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcac-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1fcac-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcac-142">입력</span><span class="sxs-lookup"><span data-stu-id="1fcac-142">INPUTS</span></span>

### <span data-ttu-id="1fcac-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1fcac-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1fcac-144">출력</span><span class="sxs-lookup"><span data-stu-id="1fcac-144">OUTPUTS</span></span>

### <span data-ttu-id="1fcac-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1fcac-145">System.Boolean</span></span>

## <span data-ttu-id="1fcac-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1fcac-146">NOTES</span></span>

<span data-ttu-id="1fcac-147">별칭</span><span class="sxs-lookup"><span data-stu-id="1fcac-147">ALIASES</span></span>

<span data-ttu-id="1fcac-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1fcac-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fcac-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fcac-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fcac-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fcac-151">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fcac-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fcac-152">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1fcac-153">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1fcac-154">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1fcac-155">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1fcac-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1fcac-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fcac-157">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1fcac-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1fcac-159">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1fcac-160">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1fcac-161">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcac-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1fcac-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fcac-162">RELATED LINKS</span></span>

