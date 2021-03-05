---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: e06cfbb595f9302bf4c7d90846e5a847a24f9322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013344"
---
# <span data-ttu-id="3d129-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="3d129-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="3d129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d129-102">SYNOPSIS</span></span>
<span data-ttu-id="3d129-103">지정된 구독, 리소스 그룹 및 모니터 이름으로 SAP 모니터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="3d129-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d129-104">SYNTAX</span></span>

### <span data-ttu-id="3d129-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d129-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d129-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d129-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d129-107">설명</span><span class="sxs-lookup"><span data-stu-id="3d129-107">DESCRIPTION</span></span>
<span data-ttu-id="3d129-108">지정된 구독, 리소스 그룹 및 모니터 이름으로 SAP 모니터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="3d129-109">예제</span><span class="sxs-lookup"><span data-stu-id="3d129-109">EXAMPLES</span></span>

### <span data-ttu-id="3d129-110">예제 1: 이름에 의해 SAP 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="3d129-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="3d129-111">이 명령은 이름으로 SAP 모니터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="3d129-112">예제 2: 개체에 따라 SAP 모니터 제거</span><span class="sxs-lookup"><span data-stu-id="3d129-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="3d129-113">이 명령은 개체에 따라 SAP 모니터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="3d129-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d129-114">PARAMETERS</span></span>

### <span data-ttu-id="3d129-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d129-115">-AsJob</span></span>
<span data-ttu-id="3d129-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3d129-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d129-117">-DefaultProfile</span></span>
<span data-ttu-id="3d129-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d129-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d129-119">-InputObject</span></span>
<span data-ttu-id="3d129-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3d129-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d129-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3d129-121">-Name</span></span>
<span data-ttu-id="3d129-122">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-122">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="3d129-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3d129-123">-NoWait</span></span>
<span data-ttu-id="3d129-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="3d129-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d129-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d129-125">-PassThru</span></span>
<span data-ttu-id="3d129-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d129-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d129-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d129-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="3d129-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d129-129">-SubscriptionId</span></span>
<span data-ttu-id="3d129-130">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d129-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3d129-132">-확인</span><span class="sxs-lookup"><span data-stu-id="3d129-132">-Confirm</span></span>
<span data-ttu-id="3d129-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d129-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d129-134">-WhatIf</span></span>
<span data-ttu-id="3d129-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d129-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d129-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d129-137">CommonParameters</span></span>
<span data-ttu-id="3d129-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d129-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d129-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d129-140">입력</span><span class="sxs-lookup"><span data-stu-id="3d129-140">INPUTS</span></span>

### <span data-ttu-id="3d129-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="3d129-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="3d129-142">출력</span><span class="sxs-lookup"><span data-stu-id="3d129-142">OUTPUTS</span></span>

### <span data-ttu-id="3d129-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d129-143">System.Boolean</span></span>

## <span data-ttu-id="3d129-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d129-144">NOTES</span></span>

<span data-ttu-id="3d129-145">별칭</span><span class="sxs-lookup"><span data-stu-id="3d129-145">ALIASES</span></span>

<span data-ttu-id="3d129-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3d129-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d129-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d129-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d129-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d129-149">INPUTOBJECT <IHanaOnAzureIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d129-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d129-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3d129-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d129-151">`[Location <String>]`: 삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="3d129-152">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="3d129-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="3d129-153">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="3d129-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3d129-155">`[ResourceName <String>]`: ID 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="3d129-156">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="3d129-157">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="3d129-158">관리 ID에 의해 확장되는 상위 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="3d129-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3d129-160">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="3d129-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3d129-161">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="3d129-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="3d129-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d129-162">RELATED LINKS</span></span>

