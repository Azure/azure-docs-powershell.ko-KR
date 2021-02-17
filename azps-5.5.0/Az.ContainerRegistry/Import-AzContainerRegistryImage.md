---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196908"
---
# <span data-ttu-id="00069-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="00069-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="00069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00069-102">SYNOPSIS</span></span>
<span data-ttu-id="00069-103">공용/Azure 레지스트리에서 Azure Container Registry로 이미지를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00069-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="00069-104">구문</span><span class="sxs-lookup"><span data-stu-id="00069-104">SYNTAX</span></span>

### <span data-ttu-id="00069-105">ImportImageByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="00069-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00069-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="00069-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00069-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="00069-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00069-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="00069-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00069-109">설명</span><span class="sxs-lookup"><span data-stu-id="00069-109">DESCRIPTION</span></span>
<span data-ttu-id="00069-110">공용/Azure 레지스트리에서 Azure Container Registry로 이미지를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00069-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="00069-111">예제</span><span class="sxs-lookup"><span data-stu-id="00069-111">EXAMPLES</span></span>

### <span data-ttu-id="00069-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="00069-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="00069-113">사용 중 상자를 ACR로 가져오기</span><span class="sxs-lookup"><span data-stu-id="00069-113">Import busybox to ACR.</span></span> <span data-ttu-id="00069-114">참고:</span><span class="sxs-lookup"><span data-stu-id="00069-114">Note:</span></span> 
* <span data-ttu-id="00069-115">원본 이미지 앞에 "library/"를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="00069-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="00069-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="00069-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="00069-117">원본 레지스트리를 공개적으로 사용할 수 없는 경우 필요한 자격 증명</span><span class="sxs-lookup"><span data-stu-id="00069-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="00069-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="00069-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="00069-119">원본 ACR에서 대상 ACR로 busybox를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00069-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="00069-120">참고:</span><span class="sxs-lookup"><span data-stu-id="00069-120">Note:</span></span> 
* <span data-ttu-id="00069-121">원본 레지스트리의 관리 사용자가 비활성화된 경우 필요한 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="00069-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00069-122">PARAMETERS</span></span>

### <span data-ttu-id="00069-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00069-123">-DefaultProfile</span></span>
<span data-ttu-id="00069-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00069-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="00069-125">-Mode</span></span>
<span data-ttu-id="00069-126">Force를 사용할 경우 기존 대상 태그를 덮어 덮어습니다.</span><span class="sxs-lookup"><span data-stu-id="00069-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="00069-127">NoForce에서 기존 대상 태그는 복사가 시작되기 전에 작업이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="00069-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="00069-128">-Password</span><span class="sxs-lookup"><span data-stu-id="00069-128">-Password</span></span>
<span data-ttu-id="00069-129">원본 레지스트리를 사용하여 인증하는 데 사용되는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="00069-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="00069-130">-RegistryName</span></span>
<span data-ttu-id="00069-131">대상 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-131">Target registry name.</span></span>

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

### <span data-ttu-id="00069-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00069-132">-ResourceGroupName</span></span>
<span data-ttu-id="00069-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-133">Resource group name.</span></span>

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

### <span data-ttu-id="00069-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="00069-134">-SourceImage</span></span>
<span data-ttu-id="00069-135">원본 이미지의 리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-135">Repository name of the source image.</span></span>

<span data-ttu-id="00069-136">리포지토리('hello-world')로 이미지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00069-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="00069-137">'latest' 태그를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00069-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="00069-138">태그로 이미지를 지정합니다('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="00069-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="00069-139">sha256 기반 매니페스트 다이제스트(' ')로 이미지를 hello-world@sha256:abc123 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00069-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="00069-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="00069-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="00069-141">원본 Azure Container Registry의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="00069-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="00069-142">-SourceRegistryUri</span></span>
<span data-ttu-id="00069-143">원본 레지스트리의 주소(예: 'mcr.microsoft.com').</span><span class="sxs-lookup"><span data-stu-id="00069-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="00069-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="00069-144">-TargetTag</span></span>
<span data-ttu-id="00069-145">form repo \[ :tag의 문자열 \] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="00069-146">태그를 생략하면 원본이 사용됩니다(또는 원본 태그도 생략된 경우 '최신').</span><span class="sxs-lookup"><span data-stu-id="00069-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="00069-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="00069-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="00069-148">매니페스트만 복사할 리포지토리 이름의 문자열 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="00069-149">태그가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00069-149">No tag will be created.</span></span>

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

### <span data-ttu-id="00069-150">-Username</span><span class="sxs-lookup"><span data-stu-id="00069-150">-Username</span></span>
<span data-ttu-id="00069-151">원본 레지스트리로 인증할 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00069-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="00069-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00069-152">-Confirm</span></span>
<span data-ttu-id="00069-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00069-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00069-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00069-154">-WhatIf</span></span>
<span data-ttu-id="00069-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="00069-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00069-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00069-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00069-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00069-157">CommonParameters</span></span>
<span data-ttu-id="00069-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00069-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00069-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00069-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00069-160">입력</span><span class="sxs-lookup"><span data-stu-id="00069-160">INPUTS</span></span>

### <span data-ttu-id="00069-161">System.String</span><span class="sxs-lookup"><span data-stu-id="00069-161">System.String</span></span>

## <span data-ttu-id="00069-162">출력</span><span class="sxs-lookup"><span data-stu-id="00069-162">OUTPUTS</span></span>

### <span data-ttu-id="00069-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00069-163">System.Boolean</span></span>

## <span data-ttu-id="00069-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00069-164">NOTES</span></span>

## <span data-ttu-id="00069-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00069-165">RELATED LINKS</span></span>
