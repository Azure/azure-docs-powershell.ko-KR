---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211756"
---
# <span data-ttu-id="ec917-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="ec917-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="ec917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec917-102">SYNOPSIS</span></span>
<span data-ttu-id="ec917-103">지정 된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대 한 공급자 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="ec917-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec917-104">SYNTAX</span></span>

### <span data-ttu-id="ec917-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec917-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ec917-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec917-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec917-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ec917-107">DESCRIPTION</span></span>
<span data-ttu-id="ec917-108">지정 된 구독, 리소스 그룹, SapMonitor 이름 및 리소스 이름에 대 한 공급자 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="ec917-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ec917-109">EXAMPLES</span></span>

### <span data-ttu-id="ec917-110">예제 1: 이름으로 SAP 모니터의 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="ec917-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="ec917-111">이 명령은 SAP 모니터의 인스턴스를 이름으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="ec917-112">예제 2: 개체 별로 SAP 모니터 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="ec917-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="ec917-113">이 명령은 SAP 모니터의 인스턴스를 개체 별로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="ec917-114">변수</span><span class="sxs-lookup"><span data-stu-id="ec917-114">PARAMETERS</span></span>

### <span data-ttu-id="ec917-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec917-115">-AsJob</span></span>
<span data-ttu-id="ec917-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ec917-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ec917-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec917-117">-DefaultProfile</span></span>
<span data-ttu-id="ec917-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec917-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec917-119">-InputObject</span></span>
<span data-ttu-id="ec917-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec917-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ec917-121">-Name</span></span>
<span data-ttu-id="ec917-122">공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec917-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec917-123">-NoWait</span></span>
<span data-ttu-id="ec917-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ec917-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec917-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec917-125">-PassThru</span></span>
<span data-ttu-id="ec917-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ec917-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec917-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec917-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="ec917-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="ec917-129">-SapMonitorName</span></span>
<span data-ttu-id="ec917-130">SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="ec917-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec917-131">-SubscriptionId</span></span>
<span data-ttu-id="ec917-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ec917-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ec917-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ec917-134">-Confirm</span></span>
<span data-ttu-id="ec917-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec917-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec917-136">-WhatIf</span></span>
<span data-ttu-id="ec917-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec917-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec917-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec917-139">CommonParameters</span></span>
<span data-ttu-id="ec917-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec917-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec917-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec917-142">입력</span><span class="sxs-lookup"><span data-stu-id="ec917-142">INPUTS</span></span>

### <span data-ttu-id="ec917-143">HanaOnAzure. IHanaOnAzureIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="ec917-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="ec917-144">출력</span><span class="sxs-lookup"><span data-stu-id="ec917-144">OUTPUTS</span></span>

### <span data-ttu-id="ec917-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ec917-145">System.Boolean</span></span>

## <span data-ttu-id="ec917-146">상속자</span><span class="sxs-lookup"><span data-stu-id="ec917-146">NOTES</span></span>

<span data-ttu-id="ec917-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="ec917-147">ALIASES</span></span>

<span data-ttu-id="ec917-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ec917-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec917-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec917-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec917-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec917-151">INPUTOBJECT <IHanaOnAzureIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec917-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec917-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="ec917-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec917-153">`[Location <String>]`: 삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="ec917-154">`[OperationKind <AccessPolicyUpdateKind?>]`: 작업 이름</span><span class="sxs-lookup"><span data-stu-id="ec917-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="ec917-155">`[ProviderInstanceName <String>]`: 공급자 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="ec917-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ec917-157">`[ResourceName <String>]`: Id 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="ec917-158">`[SapMonitorName <String>]`: SAP 모니터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="ec917-159">`[Scope <String>]`: 리소스의 리소스 공급자 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="ec917-160">관리 Id에 의해 확장 되는 부모 리소스</span><span class="sxs-lookup"><span data-stu-id="ec917-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="ec917-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ec917-162">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec917-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ec917-163">`[VaultName <String>]`: 자격 증명 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="ec917-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="ec917-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec917-164">RELATED LINKS</span></span>

