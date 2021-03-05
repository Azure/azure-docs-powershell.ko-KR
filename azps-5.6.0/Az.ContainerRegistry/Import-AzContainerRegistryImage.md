---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 675bc66afd41e5db2ee356ad45ee2fdd9b3482f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963211"
---
# <span data-ttu-id="91277-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="91277-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="91277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91277-102">SYNOPSIS</span></span>
<span data-ttu-id="91277-103">공용/azure 레지스트리에서 Azure 컨테이너 레지스트리로 이미지를 가져오습니다.</span><span class="sxs-lookup"><span data-stu-id="91277-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="91277-104">구문</span><span class="sxs-lookup"><span data-stu-id="91277-104">SYNTAX</span></span>

### <span data-ttu-id="91277-105">ImportImageByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="91277-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91277-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="91277-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91277-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="91277-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91277-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="91277-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91277-109">설명</span><span class="sxs-lookup"><span data-stu-id="91277-109">DESCRIPTION</span></span>
<span data-ttu-id="91277-110">공용/azure 레지스트리에서 Azure 컨테이너 레지스트리로 이미지를 가져오습니다.</span><span class="sxs-lookup"><span data-stu-id="91277-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="91277-111">예제</span><span class="sxs-lookup"><span data-stu-id="91277-111">EXAMPLES</span></span>

### <span data-ttu-id="91277-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="91277-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="91277-113">사용 중 상자를 ACR로 가져오기합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-113">Import busybox to ACR.</span></span> <span data-ttu-id="91277-114">참고:</span><span class="sxs-lookup"><span data-stu-id="91277-114">Note:</span></span> 
* <span data-ttu-id="91277-115">원본 이미지 앞에 "library/"를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="91277-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="91277-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="91277-117">원본 레지스트리를 공개적으로 사용할 수 없는 경우 필요한 자격 증명</span><span class="sxs-lookup"><span data-stu-id="91277-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="91277-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="91277-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="91277-119">ACR을 대상으로 하는 원본 ACR에서 busybox를 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="91277-120">참고:</span><span class="sxs-lookup"><span data-stu-id="91277-120">Note:</span></span> 
* <span data-ttu-id="91277-121">원본 레지스트리에 대한 관리자 사용자를 사용하지 않도록 설정한 경우 자격 증명이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="91277-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="91277-122">PARAMETERS</span></span>

### <span data-ttu-id="91277-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91277-123">-DefaultProfile</span></span>
<span data-ttu-id="91277-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91277-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="91277-125">-Mode</span></span>
<span data-ttu-id="91277-126">Force를 사용할 때 기존 대상 태그는 덮어 덮어 덮어 놨습니다.</span><span class="sxs-lookup"><span data-stu-id="91277-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="91277-127">NoForce가면 복사가 시작되기 전에 기존 대상 태그가 작업을 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91277-128">-Password</span><span class="sxs-lookup"><span data-stu-id="91277-128">-Password</span></span>
<span data-ttu-id="91277-129">원본 레지스트리를 사용하여 인증하는 데 사용되는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91277-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="91277-130">-RegistryName</span></span>
<span data-ttu-id="91277-131">대상 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-131">Target registry name.</span></span>

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

### <span data-ttu-id="91277-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91277-132">-ResourceGroupName</span></span>
<span data-ttu-id="91277-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-133">Resource group name.</span></span>

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

### <span data-ttu-id="91277-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="91277-134">-SourceImage</span></span>
<span data-ttu-id="91277-135">원본 이미지의 리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-135">Repository name of the source image.</span></span>

<span data-ttu-id="91277-136">리포지토리로 이미지를 지정합니다('hello-world').</span><span class="sxs-lookup"><span data-stu-id="91277-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="91277-137">이 태그는 '최신' 태그를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91277-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="91277-138">태그로 이미지를 지정합니다('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="91277-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="91277-139">sha256 기반 매니페스트 다이제스트(' ')로 이미지를 hello-world@sha256:abc123 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91277-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="91277-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="91277-141">원본 Azure Container Registry의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91277-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="91277-142">-SourceRegistryUri</span></span>
<span data-ttu-id="91277-143">원본 레지스트리의 주소(예: 'mcr.microsoft.com').</span><span class="sxs-lookup"><span data-stu-id="91277-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91277-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="91277-144">-TargetTag</span></span>
<span data-ttu-id="91277-145">폼 리포지토의 문자열 \[ 목록 \] :tag.</span><span class="sxs-lookup"><span data-stu-id="91277-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="91277-146">태그가 생략된 경우 원본이 사용됩니다(또는 원본 태그도 생략된 경우 '최신').</span><span class="sxs-lookup"><span data-stu-id="91277-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91277-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="91277-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="91277-148">매니페스트 전용 복사를 할 리포지토리 이름의 문자열 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="91277-149">태그가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91277-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91277-150">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="91277-150">-Username</span></span>
<span data-ttu-id="91277-151">원본 레지스트리를 인증하는 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91277-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91277-152">-확인</span><span class="sxs-lookup"><span data-stu-id="91277-152">-Confirm</span></span>
<span data-ttu-id="91277-153">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91277-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91277-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91277-154">-WhatIf</span></span>
<span data-ttu-id="91277-155">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="91277-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91277-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91277-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91277-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91277-157">CommonParameters</span></span>
<span data-ttu-id="91277-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91277-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91277-159">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91277-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91277-160">입력</span><span class="sxs-lookup"><span data-stu-id="91277-160">INPUTS</span></span>

### <span data-ttu-id="91277-161">System.String</span><span class="sxs-lookup"><span data-stu-id="91277-161">System.String</span></span>

## <span data-ttu-id="91277-162">출력</span><span class="sxs-lookup"><span data-stu-id="91277-162">OUTPUTS</span></span>

### <span data-ttu-id="91277-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91277-163">System.Boolean</span></span>

## <span data-ttu-id="91277-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91277-164">NOTES</span></span>

## <span data-ttu-id="91277-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91277-165">RELATED LINKS</span></span>
