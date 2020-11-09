---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304136"
---
# <span data-ttu-id="d614b-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="d614b-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="d614b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d614b-102">SYNOPSIS</span></span>
<span data-ttu-id="d614b-103">공용/azure 레지스트리에서 azure 컨테이너 레지스트리로 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="d614b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d614b-104">SYNTAX</span></span>

### <span data-ttu-id="d614b-105">ImportImageByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="d614b-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d614b-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="d614b-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d614b-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="d614b-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d614b-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="d614b-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d614b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d614b-109">DESCRIPTION</span></span>
<span data-ttu-id="d614b-110">공용/azure 레지스트리에서 azure 컨테이너 레지스트리로 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="d614b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d614b-111">EXAMPLES</span></span>

### <span data-ttu-id="d614b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d614b-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="d614b-113">Busybox를 ACR로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-113">Import busybox to ACR.</span></span> <span data-ttu-id="d614b-114">기록</span><span class="sxs-lookup"><span data-stu-id="d614b-114">Note:</span></span> 
* <span data-ttu-id="d614b-115">"library/"는 원본 이미지 앞에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="d614b-116">"busybox: 최신" => "라이브러리/busybox: 최신"</span><span class="sxs-lookup"><span data-stu-id="d614b-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="d614b-117">원본 레지스트리를 공개적으로 사용할 수 없는 경우 자격 증명이 필요 함</span><span class="sxs-lookup"><span data-stu-id="d614b-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="d614b-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="d614b-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="d614b-119">원본 ACR에서 대상 ACR로 busybox를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="d614b-120">기록</span><span class="sxs-lookup"><span data-stu-id="d614b-120">Note:</span></span> 
* <span data-ttu-id="d614b-121">원본 레지스트리의 관리자 사용자가 사용 하지 않도록 설정 된 경우 자격 증명이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="d614b-122">변수</span><span class="sxs-lookup"><span data-stu-id="d614b-122">PARAMETERS</span></span>

### <span data-ttu-id="d614b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d614b-123">-DefaultProfile</span></span>
<span data-ttu-id="d614b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d614b-125">-모드</span><span class="sxs-lookup"><span data-stu-id="d614b-125">-Mode</span></span>
<span data-ttu-id="d614b-126">강제로 실행 하면 기존의 모든 대상 태그를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="d614b-127">NoForce 때 모든 기존 대상 태그는 복사가 시작 되기 전에 작업을 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="d614b-128">-암호</span><span class="sxs-lookup"><span data-stu-id="d614b-128">-Password</span></span>
<span data-ttu-id="d614b-129">원본 레지스트리를 사용 하 여 인증 하는 데 사용 되는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="d614b-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d614b-130">-RegistryName</span></span>
<span data-ttu-id="d614b-131">대상 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-131">Target registry name.</span></span>

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

### <span data-ttu-id="d614b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d614b-132">-ResourceGroupName</span></span>
<span data-ttu-id="d614b-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-133">Resource group name.</span></span>

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

### <span data-ttu-id="d614b-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="d614b-134">-SourceImage</span></span>
<span data-ttu-id="d614b-135">원본 이미지의 리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-135">Repository name of the source image.</span></span>

<span data-ttu-id="d614b-136">리포지토리로 이미지를 지정 합니다 (' hello-월드 ').</span><span class="sxs-lookup"><span data-stu-id="d614b-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="d614b-137">' 최신 ' 태그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="d614b-138">태그 (' hello-world: 비최신 ')로 이미지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="d614b-139">Sha256 기반 매니페스트 다이제스트 (' ')를 사용 하 여 이미지를 지정 hello-world@sha256:abc123 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="d614b-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="d614b-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="d614b-141">원본 Azure 컨테이너 레지스트리의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="d614b-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="d614b-142">-SourceRegistryUri</span></span>
<span data-ttu-id="d614b-143">원본 레지스트리의 주소입니다 (예: ' mcr.microsoft.com ').</span><span class="sxs-lookup"><span data-stu-id="d614b-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="d614b-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="d614b-144">-TargetTag</span></span>
<span data-ttu-id="d614b-145">양식 리포지토리: 태그의 문자열 목록입니다 \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d614b-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="d614b-146">태그를 생략 하면 원본이 사용 됩니다 (또는 원본 태그를 생략 하는 경우에는 ' 최신 '이 라고도).</span><span class="sxs-lookup"><span data-stu-id="d614b-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="d614b-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="d614b-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="d614b-148">Manifest만 복사 하는 저장소 이름 문자열 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="d614b-149">태그가 만들어지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-149">No tag will be created.</span></span>

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

### <span data-ttu-id="d614b-150">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="d614b-150">-Username</span></span>
<span data-ttu-id="d614b-151">원본 레지스트리를 사용 하 여 인증할 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="d614b-152">-확인</span><span class="sxs-lookup"><span data-stu-id="d614b-152">-Confirm</span></span>
<span data-ttu-id="d614b-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d614b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d614b-154">-WhatIf</span></span>
<span data-ttu-id="d614b-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d614b-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d614b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d614b-157">CommonParameters</span></span>
<span data-ttu-id="d614b-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d614b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d614b-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d614b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d614b-160">입력</span><span class="sxs-lookup"><span data-stu-id="d614b-160">INPUTS</span></span>

### <span data-ttu-id="d614b-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d614b-161">System.String</span></span>

## <span data-ttu-id="d614b-162">출력</span><span class="sxs-lookup"><span data-stu-id="d614b-162">OUTPUTS</span></span>

### <span data-ttu-id="d614b-163">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d614b-163">System.Boolean</span></span>

## <span data-ttu-id="d614b-164">상속자</span><span class="sxs-lookup"><span data-stu-id="d614b-164">NOTES</span></span>

## <span data-ttu-id="d614b-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d614b-165">RELATED LINKS</span></span>
