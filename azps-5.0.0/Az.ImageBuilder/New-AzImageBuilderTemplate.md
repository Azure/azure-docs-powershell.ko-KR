---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304004"
---
# <span data-ttu-id="ae47a-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="ae47a-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="ae47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae47a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae47a-103">가상 컴퓨터 이미지 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="ae47a-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="ae47a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae47a-104">SYNTAX</span></span>

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

## <span data-ttu-id="ae47a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae47a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae47a-106">가상 컴퓨터 이미지 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="ae47a-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="ae47a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae47a-107">EXAMPLES</span></span>

### <span data-ttu-id="ae47a-108">예제 1: 가상 컴퓨터 이미지 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="ae47a-108">Example 1: Create a virtual machine image template</span></span>
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

<span data-ttu-id="ae47a-109">이 명령은 가상 컴퓨터 이미지 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="ae47a-110">변수</span><span class="sxs-lookup"><span data-stu-id="ae47a-110">PARAMETERS</span></span>

### <span data-ttu-id="ae47a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae47a-111">-AsJob</span></span>
<span data-ttu-id="ae47a-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ae47a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ae47a-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="ae47a-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="ae47a-114">이미지 템플릿을 작성 하는 동안 대기 하는 최대 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="ae47a-115">기본값 (4 시간)을 사용 하려면 0을 생략 하거나 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="ae47a-116">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="ae47a-116">-Customize</span></span>
<span data-ttu-id="ae47a-117">이미지 원본 등의 이미지 사용자 지정 단계를 설명 하는 데 사용 되는 속성을 지정 합니다. 생성 하려면 속성 사용자 지정 및 해시 테이블 만들기에 대 한 참고 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae47a-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae47a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae47a-118">-DefaultProfile</span></span>
<span data-ttu-id="ae47a-119">지역 HideParameter Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트, 구독을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae47a-120">-배포</span><span class="sxs-lookup"><span data-stu-id="ae47a-120">-Distribute</span></span>
<span data-ttu-id="ae47a-121">이미지 출력을 이동 해야 하는 배포 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="ae47a-122">생성 하려면 속성 배포 및 해시 테이블 만들기에 대 한 참고 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae47a-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae47a-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="ae47a-123">-ImageTemplateName</span></span>
<span data-ttu-id="ae47a-124">이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="ae47a-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="ae47a-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="ae47a-126">마지막 실행의 종료 시간 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="ae47a-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="ae47a-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="ae47a-128">마지막 실행 상태에 대 한 자세한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="ae47a-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="ae47a-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="ae47a-130">마지막 실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-130">State of the last run.</span></span>

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

### <span data-ttu-id="ae47a-131">-LastRunStatusRunSubState 상태</span><span class="sxs-lookup"><span data-stu-id="ae47a-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="ae47a-132">마지막 실행의 하위 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-132">Sub-state of the last run.</span></span>

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

### <span data-ttu-id="ae47a-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="ae47a-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="ae47a-134">마지막 실행의 시작 시간 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="ae47a-135">-위치</span><span class="sxs-lookup"><span data-stu-id="ae47a-135">-Location</span></span>
<span data-ttu-id="ae47a-136">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-136">Resource location.</span></span>

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

### <span data-ttu-id="ae47a-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ae47a-137">-NoWait</span></span>
<span data-ttu-id="ae47a-138">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ae47a-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae47a-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="ae47a-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="ae47a-140">프로비저닝 실패의 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-140">Error code of the provisioning failure.</span></span>

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

### <span data-ttu-id="ae47a-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ae47a-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="ae47a-142">프로비저닝 실패에 대 한 자세한 오류 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="ae47a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae47a-143">-ResourceGroupName</span></span>
<span data-ttu-id="ae47a-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae47a-145">-원본</span><span class="sxs-lookup"><span data-stu-id="ae47a-145">-Source</span></span>
<span data-ttu-id="ae47a-146">빌드, 사용자 지정 및 배포를 위한 가상 컴퓨터 이미지 원본에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="ae47a-147">생성 하려면 원본 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae47a-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae47a-148">-SubscriptionId</span></span>
<span data-ttu-id="ae47a-149">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="ae47a-150">태그</span><span class="sxs-lookup"><span data-stu-id="ae47a-150">-Tag</span></span>
<span data-ttu-id="ae47a-151">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="ae47a-151">Resource tags.</span></span>

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

### <span data-ttu-id="ae47a-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="ae47a-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="ae47a-153">사용자가 할당 한 id의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="ae47a-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="ae47a-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="ae47a-155">OS 디스크의 크기 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="ae47a-156">Azure의 기본 OS 디스크 크기를 사용 하려면 0을 생략 하거나 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="ae47a-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="ae47a-157">-VMProfileVmSize</span></span>
<span data-ttu-id="ae47a-158">이미지를 만들고, 사용자 지정 하 고, 캡처하는 데 사용 되는 가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="ae47a-159">기본값 (Standard_D1_v2)을 사용 하도록 빈 문자열을 생략 하거나 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="ae47a-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="ae47a-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="ae47a-161">이미 존재 하는 서브넷의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="ae47a-162">-확인</span><span class="sxs-lookup"><span data-stu-id="ae47a-162">-Confirm</span></span>
<span data-ttu-id="ae47a-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae47a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae47a-164">-WhatIf</span></span>
<span data-ttu-id="ae47a-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae47a-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae47a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae47a-167">CommonParameters</span></span>
<span data-ttu-id="ae47a-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae47a-169">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae47a-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae47a-170">입력</span><span class="sxs-lookup"><span data-stu-id="ae47a-170">INPUTS</span></span>

## <span data-ttu-id="ae47a-171">출력</span><span class="sxs-lookup"><span data-stu-id="ae47a-171">OUTPUTS</span></span>

### <span data-ttu-id="ae47a-172">Api20200214. IImageTemplate에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae47a-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="ae47a-173">상속자</span><span class="sxs-lookup"><span data-stu-id="ae47a-173">NOTES</span></span>

<span data-ttu-id="ae47a-174">별칭과</span><span class="sxs-lookup"><span data-stu-id="ae47a-174">ALIASES</span></span>

<span data-ttu-id="ae47a-175">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ae47a-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae47a-176">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae47a-177">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae47a-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae47a-178"><IImageTemplateCustomizer [] > 사용자 지정: 이미지 원본 등의 이미지 사용자 지정 단계를 설명 하는 데 사용 되는 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="ae47a-179">`Type <String>`: 이미지에 사용 하려는 사용자 지정 도구의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="ae47a-180">예를 들어 "Shell"은 Shell 사용자 지정자 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="ae47a-181">`[Name <String>]`:이 사용자 지정 단계에서 수행 하는 작업에 대 한 컨텍스트를 제공 하는 친근 한 이름</span><span class="sxs-lookup"><span data-stu-id="ae47a-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="ae47a-182"><배포 IImageTemplateDistributor [] >: 이미지 출력을 이동 해야 하는 배포 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="ae47a-183">`RunOutputName <String>`: 연결 된 RunOutput에 사용 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="ae47a-184">`Type <String>`: 배포 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="ae47a-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: 배포자에 의해 생성/업데이트 된 후 아티팩트에 적용 되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="ae47a-186">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="ae47a-187">원본 <IImageTemplateSource> : 빌드, 사용자 지정 및 배포를 위한 가상 컴퓨터 이미지 원본을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="ae47a-188">`Type <String>`: 시작 하려는 원본 이미지의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae47a-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="ae47a-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae47a-189">RELATED LINKS</span></span>

