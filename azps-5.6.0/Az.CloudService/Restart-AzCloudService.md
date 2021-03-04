---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956443"
---
# <span data-ttu-id="2285e-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="2285e-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="2285e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2285e-102">SYNOPSIS</span></span>
<span data-ttu-id="2285e-103">클라우드 서비스에서 하나 이상의 역할 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="2285e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2285e-104">SYNTAX</span></span>

### <span data-ttu-id="2285e-105">RestartExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="2285e-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2285e-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2285e-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2285e-107">설명</span><span class="sxs-lookup"><span data-stu-id="2285e-107">DESCRIPTION</span></span>
<span data-ttu-id="2285e-108">클라우드 서비스에서 하나 이상의 역할 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="2285e-109">예제</span><span class="sxs-lookup"><span data-stu-id="2285e-109">EXAMPLES</span></span>

### <span data-ttu-id="2285e-110">예제 1: 클라우드 서비스의 역할 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="2285e-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="2285e-111">이 명령은 ContosOrg라는 리소스 그룹에 ContosoFrontEnd_IN_0 ContosoBackEnd_IN_1 ContosoCS라는 클라우드 서비스의 2개 역할 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="2285e-112">예제 2: 클라우드 서비스의 모든 역할 다시 시작</span><span class="sxs-lookup"><span data-stu-id="2285e-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="2285e-113">이 명령은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스의 모든 역할 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="2285e-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2285e-114">PARAMETERS</span></span>

### <span data-ttu-id="2285e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2285e-115">-AsJob</span></span>
<span data-ttu-id="2285e-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2285e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2285e-117">-DefaultProfile</span></span>
<span data-ttu-id="2285e-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2285e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2285e-119">-InputObject</span></span>
<span data-ttu-id="2285e-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2285e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2285e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2285e-121">-Name</span></span>
<span data-ttu-id="2285e-122">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2285e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2285e-123">-NoWait</span></span>
<span data-ttu-id="2285e-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="2285e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2285e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2285e-125">-PassThru</span></span>
<span data-ttu-id="2285e-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2285e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2285e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2285e-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2285e-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="2285e-129">-RoleInstance</span></span>
<span data-ttu-id="2285e-130">클라우드 서비스 역할 인스턴스 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="2285e-131">'\*'의 값은 클라우드 서비스의 모든 역할 인스턴스를 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2285e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2285e-132">-SubscriptionId</span></span>
<span data-ttu-id="2285e-133">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2285e-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2285e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="2285e-135">-Confirm</span></span>
<span data-ttu-id="2285e-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2285e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2285e-137">-WhatIf</span></span>
<span data-ttu-id="2285e-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2285e-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2285e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2285e-140">CommonParameters</span></span>
<span data-ttu-id="2285e-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2285e-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2285e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2285e-143">입력</span><span class="sxs-lookup"><span data-stu-id="2285e-143">INPUTS</span></span>

### <span data-ttu-id="2285e-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="2285e-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="2285e-145">출력</span><span class="sxs-lookup"><span data-stu-id="2285e-145">OUTPUTS</span></span>

### <span data-ttu-id="2285e-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2285e-146">System.Boolean</span></span>

## <span data-ttu-id="2285e-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2285e-147">NOTES</span></span>

<span data-ttu-id="2285e-148">별칭</span><span class="sxs-lookup"><span data-stu-id="2285e-148">ALIASES</span></span>

<span data-ttu-id="2285e-149">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2285e-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2285e-150">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2285e-151">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2285e-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2285e-152">INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2285e-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2285e-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2285e-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="2285e-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2285e-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2285e-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2285e-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="2285e-156">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="2285e-157">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="2285e-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2285e-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2285e-160">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="2285e-161">업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2285e-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="2285e-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2285e-162">RELATED LINKS</span></span>

