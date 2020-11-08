---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217389"
---
# <span data-ttu-id="1ea73-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="1ea73-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="1ea73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ea73-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea73-103">패치 지정 된 구독, 리소스 그룹 및 모니터 이름에 대 한 SAP 모니터의 태그 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="1ea73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ea73-104">SYNTAX</span></span>

### <span data-ttu-id="1ea73-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ea73-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ea73-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ea73-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ea73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1ea73-107">DESCRIPTION</span></span>
<span data-ttu-id="1ea73-108">패치 지정 된 구독, 리소스 그룹 및 모니터 이름에 대 한 SAP 모니터의 태그 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="1ea73-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1ea73-109">EXAMPLES</span></span>

### <span data-ttu-id="1ea73-110">예제 1: 이름으로 SAP 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="1ea73-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="1ea73-111">이 명령은 이름으로 SAP 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="1ea73-112">예제 2: 개체 별로 SAP 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="1ea73-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="1ea73-113">이 명령은 SAP 모니터를 개체 별로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="1ea73-114">변수</span><span class="sxs-lookup"><span data-stu-id="1ea73-114">PARAMETERS</span></span>

### <span data-ttu-id="1ea73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea73-115">-DefaultProfile</span></span>
<span data-ttu-id="1ea73-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ea73-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ea73-117">-InputObject</span></span>
<span data-ttu-id="1ea73-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ea73-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1ea73-119">-Name</span></span>
<span data-ttu-id="1ea73-120">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="1ea73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea73-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ea73-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="1ea73-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ea73-123">-SubscriptionId</span></span>
<span data-ttu-id="1ea73-124">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ea73-125">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ea73-126">태그</span><span class="sxs-lookup"><span data-stu-id="1ea73-126">-Tag</span></span>
<span data-ttu-id="1ea73-127">자원의 태그 필드</span><span class="sxs-lookup"><span data-stu-id="1ea73-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="1ea73-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1ea73-128">-Confirm</span></span>
<span data-ttu-id="1ea73-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ea73-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea73-130">-WhatIf</span></span>
<span data-ttu-id="1ea73-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ea73-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ea73-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea73-133">CommonParameters</span></span>
<span data-ttu-id="1ea73-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea73-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ea73-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea73-136">입력</span><span class="sxs-lookup"><span data-stu-id="1ea73-136">INPUTS</span></span>

### <span data-ttu-id="1ea73-137">HanaOnAzure. IHanaOnAzureIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ea73-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="1ea73-138">출력</span><span class="sxs-lookup"><span data-stu-id="1ea73-138">OUTPUTS</span></span>

### <span data-ttu-id="1ea73-139">HanaOnAzure. Api20200207Preview. ISapMonitor에 대 한</span><span class="sxs-lookup"><span data-stu-id="1ea73-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="1ea73-140">상속자</span><span class="sxs-lookup"><span data-stu-id="1ea73-140">NOTES</span></span>

<span data-ttu-id="1ea73-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="1ea73-141">ALIASES</span></span>

<span data-ttu-id="1ea73-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1ea73-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ea73-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ea73-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ea73-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ea73-145">INPUTOBJECT <IHanaOnAzureIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ea73-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ea73-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1ea73-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ea73-147">`[Location <String>]`: 삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="1ea73-148">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="1ea73-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="1ea73-149">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="1ea73-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1ea73-151">`[ResourceName <String>]`: Id 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="1ea73-152">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="1ea73-153">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="1ea73-154">관리 Id에 의해 확장 되는 부모 리소스</span><span class="sxs-lookup"><span data-stu-id="1ea73-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="1ea73-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1ea73-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea73-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1ea73-157">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="1ea73-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="1ea73-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ea73-158">RELATED LINKS</span></span>

