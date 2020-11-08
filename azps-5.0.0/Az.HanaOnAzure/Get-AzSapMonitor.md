---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215347"
---
# <span data-ttu-id="0109b-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="0109b-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="0109b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0109b-102">SYNOPSIS</span></span>
<span data-ttu-id="0109b-103">지정 된 구독, 리소스 그룹 및 리소스 이름에 대 한 SAP 모니터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="0109b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0109b-104">SYNTAX</span></span>

### <span data-ttu-id="0109b-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0109b-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0109b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0109b-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0109b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0109b-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0109b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0109b-108">DESCRIPTION</span></span>
<span data-ttu-id="0109b-109">지정 된 구독, 리소스 그룹 및 리소스 이름에 대 한 SAP 모니터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="0109b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0109b-110">EXAMPLES</span></span>

### <span data-ttu-id="0109b-111">예제 1: 구독 하에 모든 SAP 모니터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0109b-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="0109b-112">이 명령은 구독 하는 동안 SAP 모니터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="0109b-113">예제 2: 이름으로 SAP 모니터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0109b-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="0109b-114">이 명령은 이름으로 SAP 모니터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="0109b-115">예제 3: 개체 별로 SAP 모니터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0109b-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="0109b-116">이 명령은 SAP 모니터를 개체 별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="0109b-117">예제 4: 파이프라인을 기준으로 SAP 모니터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0109b-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="0109b-118">이 명령은 파이프라인을 기준으로 SAP 모니터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="0109b-119">변수</span><span class="sxs-lookup"><span data-stu-id="0109b-119">PARAMETERS</span></span>

### <span data-ttu-id="0109b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0109b-120">-DefaultProfile</span></span>
<span data-ttu-id="0109b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0109b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0109b-122">-InputObject</span></span>
<span data-ttu-id="0109b-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0109b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="0109b-124">-Name</span></span>
<span data-ttu-id="0109b-125">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0109b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0109b-126">-ResourceGroupName</span></span>
<span data-ttu-id="0109b-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0109b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0109b-128">-SubscriptionId</span></span>
<span data-ttu-id="0109b-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0109b-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0109b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0109b-131">CommonParameters</span></span>
<span data-ttu-id="0109b-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0109b-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0109b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0109b-134">입력</span><span class="sxs-lookup"><span data-stu-id="0109b-134">INPUTS</span></span>

### <span data-ttu-id="0109b-135">HanaOnAzure. IHanaOnAzureIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="0109b-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="0109b-136">출력</span><span class="sxs-lookup"><span data-stu-id="0109b-136">OUTPUTS</span></span>

### <span data-ttu-id="0109b-137">HanaOnAzure. Api20200207Preview. ISapMonitor에 대 한</span><span class="sxs-lookup"><span data-stu-id="0109b-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="0109b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0109b-138">NOTES</span></span>

<span data-ttu-id="0109b-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="0109b-139">ALIASES</span></span>

<span data-ttu-id="0109b-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0109b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0109b-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0109b-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="0109b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0109b-143">INPUTOBJECT <IHanaOnAzureIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0109b-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0109b-144">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="0109b-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0109b-145">`[Location <String>]`: 삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="0109b-146">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="0109b-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="0109b-147">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="0109b-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0109b-149">`[ResourceName <String>]`: Id 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="0109b-150">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="0109b-151">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="0109b-152">관리 Id에 의해 확장 되는 부모 리소스</span><span class="sxs-lookup"><span data-stu-id="0109b-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="0109b-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0109b-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0109b-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0109b-155">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="0109b-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="0109b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0109b-156">RELATED LINKS</span></span>

