---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185825"
---
# <span data-ttu-id="4df37-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="4df37-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="4df37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df37-102">SYNOPSIS</span></span>
<span data-ttu-id="4df37-103">지정된 구독, 리소스 그룹 및 모니터 이름을 통해 SAP 모니터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="4df37-104">구문</span><span class="sxs-lookup"><span data-stu-id="4df37-104">SYNTAX</span></span>

### <span data-ttu-id="4df37-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="4df37-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4df37-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4df37-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4df37-107">설명</span><span class="sxs-lookup"><span data-stu-id="4df37-107">DESCRIPTION</span></span>
<span data-ttu-id="4df37-108">지정된 구독, 리소스 그룹 및 모니터 이름을 통해 SAP 모니터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="4df37-109">예제</span><span class="sxs-lookup"><span data-stu-id="4df37-109">EXAMPLES</span></span>

### <span data-ttu-id="4df37-110">예제 1: 이름으로 SAP 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="4df37-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="4df37-111">이 명령은 이름으로 SAP 모니터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="4df37-112">예제 2: 개체에 따라 SAP 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="4df37-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="4df37-113">이 명령은 개체에 따라 SAP 모니터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="4df37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df37-114">PARAMETERS</span></span>

### <span data-ttu-id="4df37-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4df37-115">-AsJob</span></span>
<span data-ttu-id="4df37-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4df37-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4df37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df37-117">-DefaultProfile</span></span>
<span data-ttu-id="4df37-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4df37-119">-InputObject</span></span>
<span data-ttu-id="4df37-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4df37-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4df37-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4df37-121">-Name</span></span>
<span data-ttu-id="4df37-122">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-122">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="4df37-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4df37-123">-NoWait</span></span>
<span data-ttu-id="4df37-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="4df37-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4df37-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df37-125">-PassThru</span></span>
<span data-ttu-id="4df37-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4df37-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df37-127">-ResourceGroupName</span></span>
<span data-ttu-id="4df37-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="4df37-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4df37-129">-SubscriptionId</span></span>
<span data-ttu-id="4df37-130">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4df37-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4df37-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4df37-132">-Confirm</span></span>
<span data-ttu-id="4df37-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df37-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df37-134">-WhatIf</span></span>
<span data-ttu-id="4df37-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4df37-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df37-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df37-137">CommonParameters</span></span>
<span data-ttu-id="4df37-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df37-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4df37-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df37-140">입력</span><span class="sxs-lookup"><span data-stu-id="4df37-140">INPUTS</span></span>

### <span data-ttu-id="4df37-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="4df37-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="4df37-142">출력</span><span class="sxs-lookup"><span data-stu-id="4df37-142">OUTPUTS</span></span>

### <span data-ttu-id="4df37-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4df37-143">System.Boolean</span></span>

## <span data-ttu-id="4df37-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4df37-144">NOTES</span></span>

<span data-ttu-id="4df37-145">별칭</span><span class="sxs-lookup"><span data-stu-id="4df37-145">ALIASES</span></span>

<span data-ttu-id="4df37-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4df37-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4df37-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4df37-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4df37-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4df37-149">INPUTOBJECT: <IHanaOnAzureIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4df37-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4df37-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4df37-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4df37-151">`[Location <String>]`: 삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="4df37-152">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업의 이름</span><span class="sxs-lookup"><span data-stu-id="4df37-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="4df37-153">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="4df37-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4df37-155">`[ResourceName <String>]`: ID 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="4df37-156">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="4df37-157">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="4df37-158">관리 ID에 의해 확장되는 부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="4df37-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4df37-160">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4df37-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4df37-161">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="4df37-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="4df37-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4df37-162">RELATED LINKS</span></span>

