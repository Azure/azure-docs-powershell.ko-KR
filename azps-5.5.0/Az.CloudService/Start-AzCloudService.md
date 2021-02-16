---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/start-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
ms.openlocfilehash: 2e2fe8534c1af369a8d095ba4ba3d74106700297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199412"
---
# <span data-ttu-id="5c7a0-101">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="5c7a0-101">Start-AzCloudService</span></span>

## <span data-ttu-id="5c7a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7a0-103">클라우드 서비스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-103">Starts the cloud service.</span></span>

## <span data-ttu-id="5c7a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c7a0-104">SYNTAX</span></span>

### <span data-ttu-id="5c7a0-105">시작(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c7a0-105">Start (Default)</span></span>
```
Start-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5c7a0-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c7a0-106">StartViaIdentity</span></span>
```
Start-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5c7a0-107">설명</span><span class="sxs-lookup"><span data-stu-id="5c7a0-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7a0-108">클라우드 서비스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-108">Starts the cloud service.</span></span>

## <span data-ttu-id="5c7a0-109">예제</span><span class="sxs-lookup"><span data-stu-id="5c7a0-109">EXAMPLES</span></span>

### <span data-ttu-id="5c7a0-110">예제 1: 클라우드 서비스 시작</span><span class="sxs-lookup"><span data-stu-id="5c7a0-110">Example 1: Start cloud service</span></span>
```powershell
PS C:\> Start-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="5c7a0-111">이 명령은 ContosoCS라는 클라우드 서비스에 속하는 모든 역할 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-111">This command starts all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="5c7a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c7a0-112">PARAMETERS</span></span>

### <span data-ttu-id="5c7a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c7a0-113">-AsJob</span></span>
<span data-ttu-id="5c7a0-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5c7a0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5c7a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7a0-115">-DefaultProfile</span></span>
<span data-ttu-id="5c7a0-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c7a0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c7a0-117">-InputObject</span></span>
<span data-ttu-id="5c7a0-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5c7a0-119">-Name</span></span>
<span data-ttu-id="5c7a0-120">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5c7a0-121">-NoWait</span></span>
<span data-ttu-id="5c7a0-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="5c7a0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5c7a0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c7a0-123">-PassThru</span></span>
<span data-ttu-id="5c7a0-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5c7a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c7a0-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c7a0-127">-SubscriptionId</span></span>
<span data-ttu-id="5c7a0-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5c7a0-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c7a0-130">-Confirm</span></span>
<span data-ttu-id="5c7a0-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c7a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c7a0-132">-WhatIf</span></span>
<span data-ttu-id="5c7a0-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c7a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c7a0-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c7a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7a0-135">CommonParameters</span></span>
<span data-ttu-id="5c7a0-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7a0-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7a0-138">입력</span><span class="sxs-lookup"><span data-stu-id="5c7a0-138">INPUTS</span></span>

### <span data-ttu-id="5c7a0-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5c7a0-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="5c7a0-140">출력</span><span class="sxs-lookup"><span data-stu-id="5c7a0-140">OUTPUTS</span></span>

### <span data-ttu-id="5c7a0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c7a0-141">System.Boolean</span></span>

## <span data-ttu-id="5c7a0-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c7a0-142">NOTES</span></span>

<span data-ttu-id="5c7a0-143">별칭</span><span class="sxs-lookup"><span data-stu-id="5c7a0-143">ALIASES</span></span>

<span data-ttu-id="5c7a0-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5c7a0-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c7a0-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c7a0-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c7a0-147">INPUTOBJECT: <ICloudServiceIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c7a0-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c7a0-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5c7a0-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="5c7a0-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5c7a0-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c7a0-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5c7a0-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="5c7a0-151">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="5c7a0-152">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="5c7a0-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5c7a0-154">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5c7a0-155">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="5c7a0-156">업데이트 도메인은 0부터 시작하여 식별됩니다. 첫 번째 업데이트 도메인의 ID는 0이고, 두 번째 도메인은 ID가 1인 등입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a0-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="5c7a0-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c7a0-157">RELATED LINKS</span></span>

