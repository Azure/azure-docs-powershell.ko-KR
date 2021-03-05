---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: 1f204b40bcf6cbd81449a6478d9d7d4e3f7d432d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007232"
---
# <span data-ttu-id="95753-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="95753-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="95753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95753-102">SYNOPSIS</span></span>
<span data-ttu-id="95753-103">다시 구축된 역할 인스턴스 비동기 작업은 웹 역할 또는 작업자 역할의 인스턴스에 운영 체제를 다시 설치하고, 이들이 사용하는 저장소 리소스를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="95753-104">저장소 리소스를 초기화하지 않을 경우 역할 인스턴스를 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95753-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="95753-105">구문</span><span class="sxs-lookup"><span data-stu-id="95753-105">SYNTAX</span></span>

### <span data-ttu-id="95753-106">다시빌드(기본값)</span><span class="sxs-lookup"><span data-stu-id="95753-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="95753-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="95753-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95753-108">설명</span><span class="sxs-lookup"><span data-stu-id="95753-108">DESCRIPTION</span></span>
<span data-ttu-id="95753-109">다시 구축된 역할 인스턴스 비동기 작업은 웹 역할 또는 작업자 역할의 인스턴스에 운영 체제를 다시 설치하고, 이들이 사용하는 저장소 리소스를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="95753-110">저장소 리소스를 초기화하지 않을 경우 역할 인스턴스를 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95753-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="95753-111">예제</span><span class="sxs-lookup"><span data-stu-id="95753-111">EXAMPLES</span></span>

### <span data-ttu-id="95753-112">예제 1: 클라우드 서비스의 역할 인스턴스 다시빌드</span><span class="sxs-lookup"><span data-stu-id="95753-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="95753-113">이 명령은 ContosOrg라는 리소스 그룹에 ContosoFrontEnd_IN_0 ContosoCS라는 클라우드 서비스의 역할 인스턴스를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="95753-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="95753-114">PARAMETERS</span></span>

### <span data-ttu-id="95753-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95753-115">-AsJob</span></span>
<span data-ttu-id="95753-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-116">Run the command as a job</span></span>

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

### <span data-ttu-id="95753-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="95753-117">-CloudServiceName</span></span>
<span data-ttu-id="95753-118">.</span><span class="sxs-lookup"><span data-stu-id="95753-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95753-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95753-119">-DefaultProfile</span></span>
<span data-ttu-id="95753-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95753-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95753-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95753-121">-InputObject</span></span>
<span data-ttu-id="95753-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="95753-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95753-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="95753-123">-NoWait</span></span>
<span data-ttu-id="95753-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="95753-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95753-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95753-125">-PassThru</span></span>
<span data-ttu-id="95753-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="95753-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95753-127">-ResourceGroupName</span></span>
<span data-ttu-id="95753-128">.</span><span class="sxs-lookup"><span data-stu-id="95753-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95753-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="95753-129">-RoleInstanceName</span></span>
<span data-ttu-id="95753-130">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95753-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95753-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95753-131">-SubscriptionId</span></span>
<span data-ttu-id="95753-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="95753-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="95753-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95753-134">-확인</span><span class="sxs-lookup"><span data-stu-id="95753-134">-Confirm</span></span>
<span data-ttu-id="95753-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95753-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95753-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95753-136">-WhatIf</span></span>
<span data-ttu-id="95753-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="95753-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95753-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95753-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95753-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95753-139">CommonParameters</span></span>
<span data-ttu-id="95753-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95753-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95753-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95753-142">입력</span><span class="sxs-lookup"><span data-stu-id="95753-142">INPUTS</span></span>

### <span data-ttu-id="95753-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="95753-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="95753-144">출력</span><span class="sxs-lookup"><span data-stu-id="95753-144">OUTPUTS</span></span>

### <span data-ttu-id="95753-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95753-145">System.Boolean</span></span>

## <span data-ttu-id="95753-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95753-146">NOTES</span></span>

<span data-ttu-id="95753-147">별칭</span><span class="sxs-lookup"><span data-stu-id="95753-147">ALIASES</span></span>

<span data-ttu-id="95753-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="95753-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95753-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95753-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95753-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95753-151">INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="95753-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95753-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="95753-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="95753-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="95753-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95753-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="95753-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="95753-155">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95753-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="95753-156">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95753-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="95753-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="95753-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="95753-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="95753-159">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95753-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="95753-160">업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95753-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="95753-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95753-161">RELATED LINKS</span></span>

