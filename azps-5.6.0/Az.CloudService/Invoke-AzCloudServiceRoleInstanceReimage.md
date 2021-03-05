---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965056"
---
# <span data-ttu-id="cd3c6-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="cd3c6-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="cd3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3c6-103">역할 인스턴스 다시 설치 비동기 작업은 웹 역할 또는 작업자 역할의 인스턴스에 운영 체제를 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="cd3c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd3c6-104">SYNTAX</span></span>

### <span data-ttu-id="cd3c6-105">Reimage(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd3c6-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd3c6-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd3c6-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd3c6-107">설명</span><span class="sxs-lookup"><span data-stu-id="cd3c6-107">DESCRIPTION</span></span>
<span data-ttu-id="cd3c6-108">역할 인스턴스 다시 설치 비동기 작업은 웹 역할 또는 작업자 역할의 인스턴스에 운영 체제를 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="cd3c6-109">예제</span><span class="sxs-lookup"><span data-stu-id="cd3c6-109">EXAMPLES</span></span>

### <span data-ttu-id="cd3c6-110">예제 1: 클라우드 서비스의 역할 인스턴스 다시 사용</span><span class="sxs-lookup"><span data-stu-id="cd3c6-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="cd3c6-111">이 명령은 ContosOrg라는 리소스 그룹에 ContosoFrontEnd_IN_0 ContosoCS라는 클라우드 서비스의 역할 인스턴스를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="cd3c6-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd3c6-112">PARAMETERS</span></span>

### <span data-ttu-id="cd3c6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd3c6-113">-AsJob</span></span>
<span data-ttu-id="cd3c6-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cd3c6-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="cd3c6-115">-CloudServiceName</span></span>
<span data-ttu-id="cd3c6-116">.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3c6-117">-DefaultProfile</span></span>
<span data-ttu-id="cd3c6-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd3c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd3c6-119">-InputObject</span></span>
<span data-ttu-id="cd3c6-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3c6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd3c6-121">-NoWait</span></span>
<span data-ttu-id="cd3c6-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="cd3c6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd3c6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd3c6-123">-PassThru</span></span>
<span data-ttu-id="cd3c6-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd3c6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3c6-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd3c6-126">.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3c6-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="cd3c6-127">-RoleInstanceName</span></span>
<span data-ttu-id="cd3c6-128">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3c6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd3c6-129">-SubscriptionId</span></span>
<span data-ttu-id="cd3c6-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd3c6-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3c6-132">-확인</span><span class="sxs-lookup"><span data-stu-id="cd3c6-132">-Confirm</span></span>
<span data-ttu-id="cd3c6-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd3c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd3c6-134">-WhatIf</span></span>
<span data-ttu-id="cd3c6-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd3c6-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd3c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3c6-137">CommonParameters</span></span>
<span data-ttu-id="cd3c6-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3c6-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd3c6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3c6-140">입력</span><span class="sxs-lookup"><span data-stu-id="cd3c6-140">INPUTS</span></span>

### <span data-ttu-id="cd3c6-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cd3c6-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="cd3c6-142">출력</span><span class="sxs-lookup"><span data-stu-id="cd3c6-142">OUTPUTS</span></span>

### <span data-ttu-id="cd3c6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd3c6-143">System.Boolean</span></span>

## <span data-ttu-id="cd3c6-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd3c6-144">NOTES</span></span>

<span data-ttu-id="cd3c6-145">별칭</span><span class="sxs-lookup"><span data-stu-id="cd3c6-145">ALIASES</span></span>

<span data-ttu-id="cd3c6-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cd3c6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd3c6-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd3c6-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd3c6-149">INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd3c6-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd3c6-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="cd3c6-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="cd3c6-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="cd3c6-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd3c6-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="cd3c6-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="cd3c6-153">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="cd3c6-154">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="cd3c6-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cd3c6-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cd3c6-157">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="cd3c6-158">업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="cd3c6-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd3c6-159">RELATED LINKS</span></span>

