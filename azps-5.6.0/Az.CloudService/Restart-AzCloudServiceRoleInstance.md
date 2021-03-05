---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985306"
---
# <span data-ttu-id="81d0d-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="81d0d-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="81d0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="81d0d-103">역할 인스턴스 재부팅 비동기 작업은 클라우드 서비스에서 역할 인스턴스의 재부팅을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="81d0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="81d0d-104">SYNTAX</span></span>

### <span data-ttu-id="81d0d-105">다시 시작(기본값)</span><span class="sxs-lookup"><span data-stu-id="81d0d-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81d0d-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81d0d-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81d0d-107">설명</span><span class="sxs-lookup"><span data-stu-id="81d0d-107">DESCRIPTION</span></span>
<span data-ttu-id="81d0d-108">역할 인스턴스 재부팅 비동기 작업은 클라우드 서비스에서 역할 인스턴스의 재부팅을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="81d0d-109">예제</span><span class="sxs-lookup"><span data-stu-id="81d0d-109">EXAMPLES</span></span>

### <span data-ttu-id="81d0d-110">예제 1: 클라우드 서비스의 역할 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="81d0d-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="81d0d-111">이 명령은 ContosOrg라는 리소스 그룹에 ContosoFrontEnd_IN_0 ContosoCS라는 클라우드 서비스의 역할 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="81d0d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81d0d-112">PARAMETERS</span></span>

### <span data-ttu-id="81d0d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81d0d-113">-AsJob</span></span>
<span data-ttu-id="81d0d-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="81d0d-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="81d0d-115">-CloudServiceName</span></span>
<span data-ttu-id="81d0d-116">.</span><span class="sxs-lookup"><span data-stu-id="81d0d-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d0d-117">-DefaultProfile</span></span>
<span data-ttu-id="81d0d-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d0d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81d0d-119">-InputObject</span></span>
<span data-ttu-id="81d0d-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="81d0d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d0d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="81d0d-121">-NoWait</span></span>
<span data-ttu-id="81d0d-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="81d0d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="81d0d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81d0d-123">-PassThru</span></span>
<span data-ttu-id="81d0d-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="81d0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="81d0d-126">.</span><span class="sxs-lookup"><span data-stu-id="81d0d-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d0d-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="81d0d-127">-RoleInstanceName</span></span>
<span data-ttu-id="81d0d-128">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d0d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81d0d-129">-SubscriptionId</span></span>
<span data-ttu-id="81d0d-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="81d0d-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d0d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="81d0d-132">-Confirm</span></span>
<span data-ttu-id="81d0d-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d0d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d0d-134">-WhatIf</span></span>
<span data-ttu-id="81d0d-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d0d-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d0d-137">CommonParameters</span></span>
<span data-ttu-id="81d0d-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d0d-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81d0d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d0d-140">입력</span><span class="sxs-lookup"><span data-stu-id="81d0d-140">INPUTS</span></span>

### <span data-ttu-id="81d0d-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="81d0d-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="81d0d-142">출력</span><span class="sxs-lookup"><span data-stu-id="81d0d-142">OUTPUTS</span></span>

### <span data-ttu-id="81d0d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81d0d-143">System.Boolean</span></span>

## <span data-ttu-id="81d0d-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81d0d-144">NOTES</span></span>

<span data-ttu-id="81d0d-145">별칭</span><span class="sxs-lookup"><span data-stu-id="81d0d-145">ALIASES</span></span>

<span data-ttu-id="81d0d-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="81d0d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81d0d-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81d0d-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81d0d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81d0d-149">INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="81d0d-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81d0d-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="81d0d-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="81d0d-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="81d0d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81d0d-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="81d0d-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="81d0d-153">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="81d0d-154">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="81d0d-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="81d0d-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="81d0d-157">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="81d0d-158">업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81d0d-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="81d0d-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81d0d-159">RELATED LINKS</span></span>

