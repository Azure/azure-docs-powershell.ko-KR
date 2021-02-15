---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
ms.openlocfilehash: 51fa4faa9491e4d119f3c14b1c5b44bee6fdd15e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200748"
---
# <span data-ttu-id="a5408-101">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="a5408-101">Invoke-AzCloudServiceReimage</span></span>

## <span data-ttu-id="a5408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5408-102">SYNOPSIS</span></span>
<span data-ttu-id="a5408-103">비동기 작업을 다시 설치하면 웹 역할 또는 작업 역할의 인스턴스에 운영 체제가 다시 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-103">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="a5408-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5408-104">SYNTAX</span></span>

### <span data-ttu-id="a5408-105">ReimageExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5408-105">ReimageExpanded (Default)</span></span>
```
Invoke-AzCloudServiceReimage -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a5408-106">ReimageViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a5408-106">ReimageViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceReimage -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5408-107">설명</span><span class="sxs-lookup"><span data-stu-id="a5408-107">DESCRIPTION</span></span>
<span data-ttu-id="a5408-108">비동기 작업을 다시 설치하면 웹 역할 또는 작업 역할의 인스턴스에 운영 체제가 다시 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-108">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="a5408-109">예제</span><span class="sxs-lookup"><span data-stu-id="a5408-109">EXAMPLES</span></span>

### <span data-ttu-id="a5408-110">예제 1: 클라우드 서비스의 역할 인스턴스 다시이미지</span><span class="sxs-lookup"><span data-stu-id="a5408-110">Example 1: Reimage role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="a5408-111">이 명령은 ContosOrg라는 리소스 그룹에 속한 ContosoCS라는 ContosoFrontEnd_IN_0 및 ContosoBackEnd_IN_1 서비스에서 두 역할 인스턴스를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-111">This command reimages 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="a5408-112">예제 2: 클라우드 서비스의 모든 역할 다시이미지</span><span class="sxs-lookup"><span data-stu-id="a5408-112">Example 2: Reimage all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="a5408-113">이 명령은 ContosOrg라는 리소스 그룹에 속한 ContosoCS라는 클라우드 서비스의 모든 역할 인스턴스를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-113">This command reimages all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a5408-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5408-114">PARAMETERS</span></span>

### <span data-ttu-id="a5408-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5408-115">-AsJob</span></span>
<span data-ttu-id="a5408-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5408-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a5408-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5408-117">-DefaultProfile</span></span>
<span data-ttu-id="a5408-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5408-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5408-119">-InputObject</span></span>
<span data-ttu-id="a5408-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a5408-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5408-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a5408-121">-Name</span></span>
<span data-ttu-id="a5408-122">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5408-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5408-123">-NoWait</span></span>
<span data-ttu-id="a5408-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="a5408-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5408-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5408-125">-PassThru</span></span>
<span data-ttu-id="a5408-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a5408-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5408-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5408-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5408-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="a5408-129">-RoleInstance</span></span>
<span data-ttu-id="a5408-130">클라우드 서비스 역할 인스턴스 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="a5408-131">'\*'의 값은 클라우드 서비스의 모든 역할 인스턴스를 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="a5408-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5408-132">-SubscriptionId</span></span>
<span data-ttu-id="a5408-133">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5408-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5408-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5408-135">-Confirm</span></span>
<span data-ttu-id="a5408-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5408-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5408-137">-WhatIf</span></span>
<span data-ttu-id="a5408-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5408-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5408-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5408-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5408-140">CommonParameters</span></span>
<span data-ttu-id="a5408-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5408-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5408-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5408-143">입력</span><span class="sxs-lookup"><span data-stu-id="a5408-143">INPUTS</span></span>

### <span data-ttu-id="a5408-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a5408-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="a5408-145">출력</span><span class="sxs-lookup"><span data-stu-id="a5408-145">OUTPUTS</span></span>

### <span data-ttu-id="a5408-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5408-146">System.Boolean</span></span>

## <span data-ttu-id="a5408-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5408-147">NOTES</span></span>

<span data-ttu-id="a5408-148">별칭</span><span class="sxs-lookup"><span data-stu-id="a5408-148">ALIASES</span></span>

<span data-ttu-id="a5408-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5408-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5408-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5408-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5408-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5408-152">INPUTOBJECT: <ICloudServiceIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5408-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5408-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a5408-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="a5408-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a5408-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5408-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a5408-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="a5408-156">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="a5408-157">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="a5408-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a5408-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a5408-160">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="a5408-161">업데이트 도메인은 0부터 시작하여 식별됩니다. 첫 번째 업데이트 도메인의 ID는 0이고, 두 번째 도메인은 ID가 1인 등입니다.</span><span class="sxs-lookup"><span data-stu-id="a5408-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="a5408-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5408-162">RELATED LINKS</span></span>

