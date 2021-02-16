---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 1417cc797935a532decf886f0c814ef32deee3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199401"
---
# <span data-ttu-id="ff609-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="ff609-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="ff609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff609-102">SYNOPSIS</span></span>
<span data-ttu-id="ff609-103">클라우드 서비스 전원을 끄면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-103">Power off the cloud service.</span></span>
<span data-ttu-id="ff609-104">리소스는 여전히 연결되어 있으며 리소스에 대한 요금이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="ff609-105">구문</span><span class="sxs-lookup"><span data-stu-id="ff609-105">SYNTAX</span></span>

### <span data-ttu-id="ff609-106">PowerOff(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff609-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff609-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff609-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff609-108">설명</span><span class="sxs-lookup"><span data-stu-id="ff609-108">DESCRIPTION</span></span>
<span data-ttu-id="ff609-109">클라우드 서비스 전원을 끄면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-109">Power off the cloud service.</span></span>
<span data-ttu-id="ff609-110">리소스는 여전히 연결되어 있으며 리소스에 대한 요금이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="ff609-111">예제</span><span class="sxs-lookup"><span data-stu-id="ff609-111">EXAMPLES</span></span>

### <span data-ttu-id="ff609-112">예제 1: 클라우드 서비스 중지</span><span class="sxs-lookup"><span data-stu-id="ff609-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="ff609-113">이 명령은 ContosoCS라는 클라우드 서비스에 속하는 모든 역할 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="ff609-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff609-114">PARAMETERS</span></span>

### <span data-ttu-id="ff609-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff609-115">-AsJob</span></span>
<span data-ttu-id="ff609-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ff609-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ff609-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff609-117">-DefaultProfile</span></span>
<span data-ttu-id="ff609-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff609-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff609-119">-InputObject</span></span>
<span data-ttu-id="ff609-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ff609-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff609-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ff609-121">-Name</span></span>
<span data-ttu-id="ff609-122">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff609-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ff609-123">-NoWait</span></span>
<span data-ttu-id="ff609-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ff609-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ff609-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff609-125">-PassThru</span></span>
<span data-ttu-id="ff609-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ff609-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff609-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff609-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff609-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff609-129">-SubscriptionId</span></span>
<span data-ttu-id="ff609-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff609-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff609-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff609-132">-Confirm</span></span>
<span data-ttu-id="ff609-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff609-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff609-134">-WhatIf</span></span>
<span data-ttu-id="ff609-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff609-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff609-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff609-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff609-137">CommonParameters</span></span>
<span data-ttu-id="ff609-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff609-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff609-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff609-140">입력</span><span class="sxs-lookup"><span data-stu-id="ff609-140">INPUTS</span></span>

### <span data-ttu-id="ff609-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ff609-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="ff609-142">출력</span><span class="sxs-lookup"><span data-stu-id="ff609-142">OUTPUTS</span></span>

### <span data-ttu-id="ff609-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff609-143">System.Boolean</span></span>

## <span data-ttu-id="ff609-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff609-144">NOTES</span></span>

<span data-ttu-id="ff609-145">별칭</span><span class="sxs-lookup"><span data-stu-id="ff609-145">ALIASES</span></span>

<span data-ttu-id="ff609-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ff609-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff609-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff609-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff609-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff609-149">INPUTOBJECT: <ICloudServiceIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff609-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff609-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ff609-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="ff609-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ff609-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff609-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ff609-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="ff609-153">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="ff609-154">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="ff609-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ff609-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ff609-157">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="ff609-158">업데이트 도메인은 0부터 시작하여 식별됩니다. 첫 번째 업데이트 도메인의 ID는 0이고, 두 번째 도메인은 ID가 1인 등입니다.</span><span class="sxs-lookup"><span data-stu-id="ff609-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="ff609-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff609-159">RELATED LINKS</span></span>

