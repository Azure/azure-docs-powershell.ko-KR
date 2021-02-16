---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: a37073de6a7960ae1ab90746372179db8e9d9386
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199116"
---
# <span data-ttu-id="c4117-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="c4117-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="c4117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4117-102">SYNOPSIS</span></span>
<span data-ttu-id="c4117-103">ACR 매니페스트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="c4117-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4117-104">SYNTAX</span></span>

### <span data-ttu-id="c4117-105">ByManifestParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4117-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4117-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4117-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4117-107">설명</span><span class="sxs-lookup"><span data-stu-id="c4117-107">DESCRIPTION</span></span>
<span data-ttu-id="c4117-108">ACR 매니페스트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-108">Delete ACR manifest.</span></span>
<span data-ttu-id="c4117-109">이 cmdlet을 사용 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="c4117-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="c4117-110">먼저</span><span class="sxs-lookup"><span data-stu-id="c4117-110">first.</span></span>

## <span data-ttu-id="c4117-111">예제</span><span class="sxs-lookup"><span data-stu-id="c4117-111">EXAMPLES</span></span>

### <span data-ttu-id="c4117-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4117-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="c4117-113">레지스트리에서 매니페스트 sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="c4117-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c4117-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="c4117-115">레지스트리에서 리포지토리 테스트/busybox27에 대한 태그가 있는 매니페스트 삭제</span><span class="sxs-lookup"><span data-stu-id="c4117-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="c4117-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4117-116">PARAMETERS</span></span>

### <span data-ttu-id="c4117-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4117-117">-DefaultProfile</span></span>
<span data-ttu-id="c4117-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4117-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="c4117-119">-Manifest</span></span>
<span data-ttu-id="c4117-120">매니페스트 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4117-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c4117-121">-RegistryName</span></span>
<span data-ttu-id="c4117-122">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c4117-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="c4117-123">-RepositoryName</span></span>
<span data-ttu-id="c4117-124">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-124">Repository Name.</span></span>

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

### <span data-ttu-id="c4117-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4117-125">-Tag</span></span>
<span data-ttu-id="c4117-126">태그.</span><span class="sxs-lookup"><span data-stu-id="c4117-126">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4117-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4117-127">-Confirm</span></span>
<span data-ttu-id="c4117-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4117-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4117-129">-WhatIf</span></span>
<span data-ttu-id="c4117-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4117-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4117-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4117-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4117-132">CommonParameters</span></span>
<span data-ttu-id="c4117-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4117-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4117-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4117-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4117-135">입력</span><span class="sxs-lookup"><span data-stu-id="c4117-135">INPUTS</span></span>

### <span data-ttu-id="c4117-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c4117-136">System.String</span></span>

## <span data-ttu-id="c4117-137">출력</span><span class="sxs-lookup"><span data-stu-id="c4117-137">OUTPUTS</span></span>

### <span data-ttu-id="c4117-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4117-138">System.Boolean</span></span>

## <span data-ttu-id="c4117-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4117-139">NOTES</span></span>

## <span data-ttu-id="c4117-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4117-140">RELATED LINKS</span></span>
