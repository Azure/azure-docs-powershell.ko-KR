---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 223884fb5974c94b31d8d3ddf2017e1c6e3740b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013323"
---
# <span data-ttu-id="a2f03-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="a2f03-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="a2f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f03-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f03-103">지정된 구독, 리소스 그룹 및 모니터 이름에 대한 SAP 모니터의 태그 필드를 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="a2f03-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2f03-104">SYNTAX</span></span>

### <span data-ttu-id="a2f03-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a2f03-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2f03-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a2f03-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2f03-107">설명</span><span class="sxs-lookup"><span data-stu-id="a2f03-107">DESCRIPTION</span></span>
<span data-ttu-id="a2f03-108">지정된 구독, 리소스 그룹 및 모니터 이름에 대한 SAP 모니터의 태그 필드를 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="a2f03-109">예제</span><span class="sxs-lookup"><span data-stu-id="a2f03-109">EXAMPLES</span></span>

### <span data-ttu-id="a2f03-110">예제 1: 이름에 의해 SAP 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="a2f03-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="a2f03-111">이 명령은 SAP 모니터를 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="a2f03-112">예제 2: 개체에 따라 SAP 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="a2f03-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="a2f03-113">이 명령은 개체에 따라 SAP 모니터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="a2f03-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2f03-114">PARAMETERS</span></span>

### <span data-ttu-id="a2f03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f03-115">-DefaultProfile</span></span>
<span data-ttu-id="a2f03-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2f03-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2f03-117">-InputObject</span></span>
<span data-ttu-id="a2f03-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a2f03-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2f03-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a2f03-119">-Name</span></span>
<span data-ttu-id="a2f03-120">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="a2f03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f03-121">-ResourceGroupName</span></span>
<span data-ttu-id="a2f03-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="a2f03-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2f03-123">-SubscriptionId</span></span>
<span data-ttu-id="a2f03-124">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a2f03-125">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a2f03-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2f03-126">-Tag</span></span>
<span data-ttu-id="a2f03-127">리소스의 태그 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="a2f03-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a2f03-128">-Confirm</span></span>
<span data-ttu-id="a2f03-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f03-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f03-130">-WhatIf</span></span>
<span data-ttu-id="a2f03-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2f03-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f03-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f03-133">CommonParameters</span></span>
<span data-ttu-id="a2f03-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f03-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2f03-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f03-136">입력</span><span class="sxs-lookup"><span data-stu-id="a2f03-136">INPUTS</span></span>

### <span data-ttu-id="a2f03-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="a2f03-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="a2f03-138">출력</span><span class="sxs-lookup"><span data-stu-id="a2f03-138">OUTPUTS</span></span>

### <span data-ttu-id="a2f03-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="a2f03-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="a2f03-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2f03-140">NOTES</span></span>

<span data-ttu-id="a2f03-141">별칭</span><span class="sxs-lookup"><span data-stu-id="a2f03-141">ALIASES</span></span>

<span data-ttu-id="a2f03-142">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a2f03-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2f03-143">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2f03-144">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2f03-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2f03-145">INPUTOBJECT <IHanaOnAzureIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2f03-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2f03-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a2f03-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2f03-147">`[Location <String>]`: 삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="a2f03-148">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="a2f03-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="a2f03-149">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="a2f03-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a2f03-151">`[ResourceName <String>]`: ID 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="a2f03-152">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="a2f03-153">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="a2f03-154">관리 ID에 의해 확장되는 상위 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="a2f03-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a2f03-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f03-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a2f03-157">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="a2f03-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="a2f03-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2f03-158">RELATED LINKS</span></span>

