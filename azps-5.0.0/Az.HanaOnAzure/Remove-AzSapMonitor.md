---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215341"
---
# <span data-ttu-id="aa55e-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="aa55e-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="aa55e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa55e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa55e-103">지정 된 구독, 리소스 그룹 및 모니터 이름을 사용 하 여 SAP 모니터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="aa55e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa55e-104">SYNTAX</span></span>

### <span data-ttu-id="aa55e-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="aa55e-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa55e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa55e-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa55e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aa55e-107">DESCRIPTION</span></span>
<span data-ttu-id="aa55e-108">지정 된 구독, 리소스 그룹 및 모니터 이름을 사용 하 여 SAP 모니터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="aa55e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aa55e-109">EXAMPLES</span></span>

### <span data-ttu-id="aa55e-110">예제 1: 이름으로 SAP 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="aa55e-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="aa55e-111">이 명령은 이름으로 SAP 모니터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="aa55e-112">예제 2: 개체 별로 SAP 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="aa55e-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="aa55e-113">이 명령은 SAP 모니터를 개체 별로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="aa55e-114">변수</span><span class="sxs-lookup"><span data-stu-id="aa55e-114">PARAMETERS</span></span>

### <span data-ttu-id="aa55e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa55e-115">-AsJob</span></span>
<span data-ttu-id="aa55e-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="aa55e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aa55e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa55e-117">-DefaultProfile</span></span>
<span data-ttu-id="aa55e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa55e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa55e-119">-InputObject</span></span>
<span data-ttu-id="aa55e-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa55e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="aa55e-121">-Name</span></span>
<span data-ttu-id="aa55e-122">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa55e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aa55e-123">-NoWait</span></span>
<span data-ttu-id="aa55e-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="aa55e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aa55e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa55e-125">-PassThru</span></span>
<span data-ttu-id="aa55e-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aa55e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa55e-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa55e-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="aa55e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa55e-129">-SubscriptionId</span></span>
<span data-ttu-id="aa55e-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa55e-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aa55e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="aa55e-132">-Confirm</span></span>
<span data-ttu-id="aa55e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa55e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa55e-134">-WhatIf</span></span>
<span data-ttu-id="aa55e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa55e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa55e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa55e-137">CommonParameters</span></span>
<span data-ttu-id="aa55e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa55e-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa55e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa55e-140">입력</span><span class="sxs-lookup"><span data-stu-id="aa55e-140">INPUTS</span></span>

### <span data-ttu-id="aa55e-141">HanaOnAzure. IHanaOnAzureIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa55e-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="aa55e-142">출력</span><span class="sxs-lookup"><span data-stu-id="aa55e-142">OUTPUTS</span></span>

### <span data-ttu-id="aa55e-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="aa55e-143">System.Boolean</span></span>

## <span data-ttu-id="aa55e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="aa55e-144">NOTES</span></span>

<span data-ttu-id="aa55e-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="aa55e-145">ALIASES</span></span>

<span data-ttu-id="aa55e-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="aa55e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa55e-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa55e-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa55e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa55e-149">INPUTOBJECT <IHanaOnAzureIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa55e-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa55e-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="aa55e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa55e-151">`[Location <String>]`: 삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="aa55e-152">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="aa55e-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="aa55e-153">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="aa55e-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="aa55e-155">`[ResourceName <String>]`: Id 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="aa55e-156">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="aa55e-157">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="aa55e-158">관리 Id에 의해 확장 되는 부모 리소스</span><span class="sxs-lookup"><span data-stu-id="aa55e-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="aa55e-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aa55e-160">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa55e-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aa55e-161">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="aa55e-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="aa55e-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa55e-162">RELATED LINKS</span></span>

