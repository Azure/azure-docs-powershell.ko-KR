---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048213"
---
# <span data-ttu-id="2221c-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="2221c-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="2221c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2221c-102">SYNOPSIS</span></span>
<span data-ttu-id="2221c-103">Kusto principalAssignment을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="2221c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2221c-104">SYNTAX</span></span>

### <span data-ttu-id="2221c-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2221c-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2221c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2221c-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2221c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2221c-107">DESCRIPTION</span></span>
<span data-ttu-id="2221c-108">Kusto principalAssignment을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="2221c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2221c-109">EXAMPLES</span></span>

### <span data-ttu-id="2221c-110">예제 1: 이름으로 기존 Kusto 데이터베이스 PrincipalAssignment 삭제</span><span class="sxs-lookup"><span data-stu-id="2221c-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="2221c-111">위의 명령은 Kusto database "mykustodatabase"에서 "kustoprincipal1" 이라는 PrincipalAssignment을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="2221c-112">변수</span><span class="sxs-lookup"><span data-stu-id="2221c-112">PARAMETERS</span></span>

### <span data-ttu-id="2221c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2221c-113">-AsJob</span></span>
<span data-ttu-id="2221c-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2221c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2221c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2221c-115">-ClusterName</span></span>
<span data-ttu-id="2221c-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2221c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2221c-117">-DatabaseName</span></span>
<span data-ttu-id="2221c-118">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="2221c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2221c-119">-DefaultProfile</span></span>
<span data-ttu-id="2221c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2221c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2221c-121">-InputObject</span></span>
<span data-ttu-id="2221c-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2221c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2221c-123">-NoWait</span></span>
<span data-ttu-id="2221c-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2221c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2221c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2221c-125">-PassThru</span></span>
<span data-ttu-id="2221c-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2221c-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2221c-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="2221c-128">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="2221c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2221c-129">-ResourceGroupName</span></span>
<span data-ttu-id="2221c-130">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2221c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2221c-131">-SubscriptionId</span></span>
<span data-ttu-id="2221c-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2221c-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2221c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="2221c-134">-Confirm</span></span>
<span data-ttu-id="2221c-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2221c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2221c-136">-WhatIf</span></span>
<span data-ttu-id="2221c-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2221c-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2221c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2221c-139">CommonParameters</span></span>
<span data-ttu-id="2221c-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2221c-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2221c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2221c-142">입력</span><span class="sxs-lookup"><span data-stu-id="2221c-142">INPUTS</span></span>

### <span data-ttu-id="2221c-143">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="2221c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2221c-144">출력</span><span class="sxs-lookup"><span data-stu-id="2221c-144">OUTPUTS</span></span>

### <span data-ttu-id="2221c-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2221c-145">System.Boolean</span></span>

## <span data-ttu-id="2221c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="2221c-146">NOTES</span></span>

<span data-ttu-id="2221c-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="2221c-147">ALIASES</span></span>

<span data-ttu-id="2221c-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2221c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2221c-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2221c-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="2221c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2221c-151">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2221c-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2221c-152">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2221c-153">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2221c-154">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2221c-155">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2221c-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="2221c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2221c-157">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="2221c-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2221c-158">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2221c-159">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2221c-160">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2221c-161">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2221c-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2221c-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2221c-162">RELATED LINKS</span></span>

