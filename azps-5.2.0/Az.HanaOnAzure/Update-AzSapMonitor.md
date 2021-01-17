---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342141"
---
# <span data-ttu-id="e8ce2-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="e8ce2-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="e8ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ce2-103">지정된 구독, 리소스 그룹 및 모니터 이름에 대한 SAP 모니터의 태그 필드를 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="e8ce2-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8ce2-104">SYNTAX</span></span>

### <span data-ttu-id="e8ce2-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8ce2-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e8ce2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e8ce2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8ce2-107">설명</span><span class="sxs-lookup"><span data-stu-id="e8ce2-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ce2-108">지정된 구독, 리소스 그룹 및 모니터 이름에 대한 SAP 모니터의 태그 필드를 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="e8ce2-109">예제</span><span class="sxs-lookup"><span data-stu-id="e8ce2-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ce2-110">예제 1: 이름으로 SAP 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8ce2-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="e8ce2-111">이 명령은 이름으로 SAP 모니터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="e8ce2-112">예제 2: 개체에 따라 SAP 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8ce2-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="e8ce2-113">이 명령은 개체에 따라 SAP 모니터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="e8ce2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8ce2-114">PARAMETERS</span></span>

### <span data-ttu-id="e8ce2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ce2-115">-DefaultProfile</span></span>
<span data-ttu-id="e8ce2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ce2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ce2-117">-InputObject</span></span>
<span data-ttu-id="e8ce2-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e8ce2-119">-Name</span></span>
<span data-ttu-id="e8ce2-120">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ce2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8ce2-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-122">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce2-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8ce2-123">-SubscriptionId</span></span>
<span data-ttu-id="e8ce2-124">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e8ce2-125">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce2-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8ce2-126">-Tag</span></span>
<span data-ttu-id="e8ce2-127">리소스의 태그 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-127">Tags field of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8ce2-128">-Confirm</span></span>
<span data-ttu-id="e8ce2-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ce2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ce2-130">-WhatIf</span></span>
<span data-ttu-id="e8ce2-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e8ce2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ce2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ce2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ce2-133">CommonParameters</span></span>
<span data-ttu-id="e8ce2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ce2-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ce2-136">입력</span><span class="sxs-lookup"><span data-stu-id="e8ce2-136">INPUTS</span></span>

### <span data-ttu-id="e8ce2-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="e8ce2-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="e8ce2-138">출력</span><span class="sxs-lookup"><span data-stu-id="e8ce2-138">OUTPUTS</span></span>

### <span data-ttu-id="e8ce2-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="e8ce2-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="e8ce2-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8ce2-140">NOTES</span></span>

<span data-ttu-id="e8ce2-141">별칭</span><span class="sxs-lookup"><span data-stu-id="e8ce2-141">ALIASES</span></span>

<span data-ttu-id="e8ce2-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e8ce2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8ce2-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8ce2-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8ce2-145">INPUTOBJECT: <IHanaOnAzureIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8ce2-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8ce2-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e8ce2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8ce2-147">`[Location <String>]`: 삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="e8ce2-148">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업의 이름</span><span class="sxs-lookup"><span data-stu-id="e8ce2-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="e8ce2-149">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="e8ce2-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e8ce2-151">`[ResourceName <String>]`: ID 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="e8ce2-152">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="e8ce2-153">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="e8ce2-154">관리 ID에 의해 확장되는 부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="e8ce2-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e8ce2-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ce2-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e8ce2-157">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="e8ce2-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="e8ce2-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8ce2-158">RELATED LINKS</span></span>

