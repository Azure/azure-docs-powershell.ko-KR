---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 98ef058c8a5110f7b97d794f7ebf41744ac12c2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013035"
---
# <span data-ttu-id="8a6a0-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="8a6a0-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="8a6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6a0-103">가상 머신 이미지 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="8a6a0-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="8a6a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a6a0-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a6a0-105">설명</span><span class="sxs-lookup"><span data-stu-id="8a6a0-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6a0-106">가상 머신 이미지 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="8a6a0-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="8a6a0-107">예제</span><span class="sxs-lookup"><span data-stu-id="8a6a0-107">EXAMPLES</span></span>

### <span data-ttu-id="8a6a0-108">예제 1: 가상 머신 이미지 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="8a6a0-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="8a6a0-109">이 명령은 가상 머신 이미지 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="8a6a0-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a6a0-110">PARAMETERS</span></span>

### <span data-ttu-id="8a6a0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a6a0-111">-AsJob</span></span>
<span data-ttu-id="8a6a0-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8a6a0-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="8a6a0-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="8a6a0-114">이미지 템플릿을 작성하는 동안 대기하는 최대 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="8a6a0-115">기본값(4시간)을 사용할 0을 생략하거나 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-115">Omit or specify 0 to use the default (4 hours).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-116">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="8a6a0-116">-Customize</span></span>
<span data-ttu-id="8a6a0-117">이미지 원본 등 이미지의 사용자 지정 단계를 설명하는 데 사용되는 속성을 지정합니다. 생성을 위해 사용자 지정 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6a0-118">-DefaultProfile</span></span>
<span data-ttu-id="8a6a0-119">region HideParameter Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6a0-120">-배포</span><span class="sxs-lookup"><span data-stu-id="8a6a0-120">-Distribute</span></span>
<span data-ttu-id="8a6a0-121">이미지 출력으로 이동해야 하는 배포 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="8a6a0-122">생성을 위해 DISTRIBUTE 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="8a6a0-123">-ImageTemplateName</span></span>
<span data-ttu-id="8a6a0-124">이미지 템플릿의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="8a6a0-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="8a6a0-126">마지막 실행(UTC)의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="8a6a0-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="8a6a0-128">마지막 실행 상태의 자세한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-128">Verbose information about the last run state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="8a6a0-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="8a6a0-130">마지막 실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="8a6a0-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="8a6a0-132">마지막 실행의 하위 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="8a6a0-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="8a6a0-134">마지막 실행(UTC)의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-135">-Location</span><span class="sxs-lookup"><span data-stu-id="8a6a0-135">-Location</span></span>
<span data-ttu-id="8a6a0-136">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-136">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8a6a0-137">-NoWait</span></span>
<span data-ttu-id="8a6a0-138">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="8a6a0-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8a6a0-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="8a6a0-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="8a6a0-140">프로비전 오류의 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="8a6a0-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="8a6a0-142">프로비전 오류에 대한 자세한 오류 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-142">Verbose error message about the provisioning failure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6a0-143">-ResourceGroupName</span></span>
<span data-ttu-id="8a6a0-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-145">-Source</span><span class="sxs-lookup"><span data-stu-id="8a6a0-145">-Source</span></span>
<span data-ttu-id="8a6a0-146">구축, 사용자 지정 및 배포를 위한 가상 머신 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="8a6a0-147">생성을 위해 SOURCE 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a6a0-148">-SubscriptionId</span></span>
<span data-ttu-id="8a6a0-149">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a6a0-150">-Tag</span></span>
<span data-ttu-id="8a6a0-151">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-151">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="8a6a0-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="8a6a0-153">사용자 할당 ID의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-153">The id of user assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="8a6a0-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="8a6a0-155">GB의 OS 디스크 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="8a6a0-156">Azure의 기본 OS 디스크 크기를 사용할 0을 생략하거나 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="8a6a0-157">-VMProfileVmSize</span></span>
<span data-ttu-id="8a6a0-158">이미지를 빌드, 사용자 지정 및 캡처하는 데 사용되는 가상 머신의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="8a6a0-159">기본값을 사용할 빈 문자열을 생략하거나 지정합니다(Standard_D1_v2.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="8a6a0-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="8a6a0-161">기존 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-161">Resource id of a pre-existing subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6a0-162">-확인</span><span class="sxs-lookup"><span data-stu-id="8a6a0-162">-Confirm</span></span>
<span data-ttu-id="8a6a0-163">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6a0-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6a0-164">-WhatIf</span></span>
<span data-ttu-id="8a6a0-165">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a6a0-166">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6a0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6a0-167">CommonParameters</span></span>
<span data-ttu-id="8a6a0-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6a0-169">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a6a0-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6a0-170">입력</span><span class="sxs-lookup"><span data-stu-id="8a6a0-170">INPUTS</span></span>

## <span data-ttu-id="8a6a0-171">출력</span><span class="sxs-lookup"><span data-stu-id="8a6a0-171">OUTPUTS</span></span>

### <span data-ttu-id="8a6a0-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="8a6a0-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="8a6a0-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a6a0-173">NOTES</span></span>

<span data-ttu-id="8a6a0-174">별칭</span><span class="sxs-lookup"><span data-stu-id="8a6a0-174">ALIASES</span></span>

<span data-ttu-id="8a6a0-175">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8a6a0-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a6a0-176">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a6a0-177">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a6a0-178">CUSTOM <IImageTemplateCustomizer[]>: 이미지 원본 등 이미지의 사용자 지정 단계를 설명하는 데 사용되는 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="8a6a0-179">`Type <String>`: 이미지에서 사용할 사용자 지정 도구의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="8a6a0-180">예를 들어 "Shell"은 셸 사용자 지정자일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="8a6a0-181">`[Name <String>]`: 이 사용자 지정 단계가 하는 일에 대한 컨텍스트를 제공하는 친숙한 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a0-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="8a6a0-182">배포 <IImageTemplateDistributor[]>: 이미지 출력으로 이동해야 하는 배포 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="8a6a0-183">`RunOutputName <String>`: 연결된 RunOutput에 사용할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="8a6a0-184">`Type <String>`: 배포 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="8a6a0-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: 배포자가 생성/업데이트한 후 아티팩트에 적용될 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="8a6a0-186">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="8a6a0-187">원본 : 구축, 사용자 지정 및 배포를 위한 가상 <IImageTemplateSource> 머신 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="8a6a0-188">`Type <String>`: 시작할 원본 이미지의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a0-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="8a6a0-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a6a0-189">RELATED LINKS</span></span>

