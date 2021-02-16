---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203971"
---
# <span data-ttu-id="b0a2e-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="b0a2e-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="b0a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a2e-103">지정된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대한 공급자 인스턴스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="b0a2e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0a2e-104">SYNTAX</span></span>

### <span data-ttu-id="b0a2e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b0a2e-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0a2e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b0a2e-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0a2e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0a2e-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0a2e-108">설명</span><span class="sxs-lookup"><span data-stu-id="b0a2e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0a2e-109">지정된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대한 공급자 인스턴스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="b0a2e-110">예제</span><span class="sxs-lookup"><span data-stu-id="b0a2e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0a2e-111">예제 1: SAP 모니터에서 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b0a2e-112">이 명령은 SAP 모니터에서 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="b0a2e-113">예제 2: 이름으로 SAP 모니터의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b0a2e-114">이 명령은 이름으로 SAP 모니터의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="b0a2e-115">예제 3: 개체로 SAP 모니터의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b0a2e-116">이 명령은 개체에 따라 SAP 모니터의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="b0a2e-117">예제 4: 파이프라인으로 SAP 모니터의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="b0a2e-118">이 명령은 파이프라인에 의해 SAP 모니터의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="b0a2e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0a2e-119">PARAMETERS</span></span>

### <span data-ttu-id="b0a2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a2e-120">-DefaultProfile</span></span>
<span data-ttu-id="b0a2e-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a2e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0a2e-122">-InputObject</span></span>
<span data-ttu-id="b0a2e-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a2e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b0a2e-124">-Name</span></span>
<span data-ttu-id="b0a2e-125">공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0a2e-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a2e-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="b0a2e-128">-SapMonitorName</span></span>
<span data-ttu-id="b0a2e-129">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a2e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0a2e-130">-SubscriptionId</span></span>
<span data-ttu-id="b0a2e-131">Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0a2e-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a2e-133">CommonParameters</span></span>
<span data-ttu-id="b0a2e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a2e-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a2e-136">입력</span><span class="sxs-lookup"><span data-stu-id="b0a2e-136">INPUTS</span></span>

### <span data-ttu-id="b0a2e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="b0a2e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="b0a2e-138">출력</span><span class="sxs-lookup"><span data-stu-id="b0a2e-138">OUTPUTS</span></span>

### <span data-ttu-id="b0a2e-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="b0a2e-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="b0a2e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0a2e-140">NOTES</span></span>

<span data-ttu-id="b0a2e-141">별칭</span><span class="sxs-lookup"><span data-stu-id="b0a2e-141">ALIASES</span></span>

<span data-ttu-id="b0a2e-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b0a2e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0a2e-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0a2e-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0a2e-145">INPUTOBJECT: <IHanaOnAzureIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0a2e-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0a2e-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b0a2e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0a2e-147">`[Location <String>]`: 삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="b0a2e-148">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업의 이름</span><span class="sxs-lookup"><span data-stu-id="b0a2e-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="b0a2e-149">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="b0a2e-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b0a2e-151">`[ResourceName <String>]`: ID 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="b0a2e-152">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="b0a2e-153">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="b0a2e-154">관리 ID에 의해 확장되는 부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="b0a2e-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0a2e-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a2e-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b0a2e-157">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="b0a2e-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="b0a2e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0a2e-158">RELATED LINKS</span></span>

