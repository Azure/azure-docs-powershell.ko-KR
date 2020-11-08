---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213382"
---
# <span data-ttu-id="f4d04-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f4d04-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="f4d04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d04-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d04-103">지정 된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대 한 공급자 인스턴스의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f4d04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4d04-104">SYNTAX</span></span>

### <span data-ttu-id="f4d04-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4d04-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4d04-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f4d04-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4d04-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4d04-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d04-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f4d04-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d04-109">지정 된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대 한 공급자 인스턴스의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f4d04-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f4d04-110">EXAMPLES</span></span>

### <span data-ttu-id="f4d04-111">예제 1: SAP 모니터 아래에 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4d04-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f4d04-112">이 명령은 SAP 모니터 아래에 있는 모든 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="f4d04-113">예제 2: 이름별로 SAP 모니터의 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4d04-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f4d04-114">이 명령은 이름으로 SAP 모니터의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="f4d04-115">예제 3: 개체 별로 SAP 모니터의 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4d04-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f4d04-116">이 명령은 SAP 모니터의 인스턴스를 개체 별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="f4d04-117">예제 4: 파이프라인에 따라 SAP 모니터의 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4d04-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f4d04-118">이 명령은 파이프라인 별로 SAP 모니터의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="f4d04-119">변수</span><span class="sxs-lookup"><span data-stu-id="f4d04-119">PARAMETERS</span></span>

### <span data-ttu-id="f4d04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d04-120">-DefaultProfile</span></span>
<span data-ttu-id="f4d04-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d04-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4d04-122">-InputObject</span></span>
<span data-ttu-id="f4d04-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4d04-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f4d04-124">-Name</span></span>
<span data-ttu-id="f4d04-125">공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="f4d04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d04-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4d04-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="f4d04-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="f4d04-128">-SapMonitorName</span></span>
<span data-ttu-id="f4d04-129">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f4d04-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4d04-130">-SubscriptionId</span></span>
<span data-ttu-id="f4d04-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4d04-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f4d04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d04-133">CommonParameters</span></span>
<span data-ttu-id="f4d04-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d04-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4d04-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d04-136">입력</span><span class="sxs-lookup"><span data-stu-id="f4d04-136">INPUTS</span></span>

### <span data-ttu-id="f4d04-137">HanaOnAzure. IHanaOnAzureIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4d04-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f4d04-138">출력</span><span class="sxs-lookup"><span data-stu-id="f4d04-138">OUTPUTS</span></span>

### <span data-ttu-id="f4d04-139">HanaOnAzure. Api20200207Preview. IProviderInstance에 대 한</span><span class="sxs-lookup"><span data-stu-id="f4d04-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="f4d04-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f4d04-140">NOTES</span></span>

<span data-ttu-id="f4d04-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="f4d04-141">ALIASES</span></span>

<span data-ttu-id="f4d04-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f4d04-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4d04-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4d04-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4d04-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4d04-145">INPUTOBJECT <IHanaOnAzureIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4d04-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4d04-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="f4d04-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4d04-147">`[Location <String>]`: 삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f4d04-148">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="f4d04-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f4d04-149">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f4d04-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f4d04-151">`[ResourceName <String>]`: Id 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f4d04-152">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f4d04-153">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f4d04-154">관리 Id에 의해 확장 되는 부모 리소스</span><span class="sxs-lookup"><span data-stu-id="f4d04-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f4d04-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4d04-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d04-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f4d04-157">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="f4d04-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f4d04-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4d04-158">RELATED LINKS</span></span>

