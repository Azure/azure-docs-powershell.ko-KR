---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963163"
---
# <span data-ttu-id="47b45-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="47b45-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="47b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b45-102">SYNOPSIS</span></span>
<span data-ttu-id="47b45-103">ACR 매니페스트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="47b45-104">구문</span><span class="sxs-lookup"><span data-stu-id="47b45-104">SYNTAX</span></span>

### <span data-ttu-id="47b45-105">ByManifestParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="47b45-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b45-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b45-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b45-107">설명</span><span class="sxs-lookup"><span data-stu-id="47b45-107">DESCRIPTION</span></span>
<span data-ttu-id="47b45-108">ACR 매니페스트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-108">Delete ACR manifest.</span></span>
<span data-ttu-id="47b45-109">이 cmdlet을 사용 하시기 바랍니다. `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="47b45-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="47b45-110">먼저.</span><span class="sxs-lookup"><span data-stu-id="47b45-110">first.</span></span>

## <span data-ttu-id="47b45-111">예제</span><span class="sxs-lookup"><span data-stu-id="47b45-111">EXAMPLES</span></span>

### <span data-ttu-id="47b45-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="47b45-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="47b45-113">매니페스트 sha256:31a54a0cf86d7354788a8265f60ae6acb348a67efbcf7c1007ddd3cf7af05ab 아래 레지스트리에서 매니페스트 테스트/busybox27</span><span class="sxs-lookup"><span data-stu-id="47b45-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="47b45-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="47b45-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="47b45-115">레지스트리에서 리포지토리 테스트/busybox27에 대한 태그 최신 매니페스트 삭제</span><span class="sxs-lookup"><span data-stu-id="47b45-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="47b45-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="47b45-116">PARAMETERS</span></span>

### <span data-ttu-id="47b45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b45-117">-DefaultProfile</span></span>
<span data-ttu-id="47b45-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b45-119">-매니페스트</span><span class="sxs-lookup"><span data-stu-id="47b45-119">-Manifest</span></span>
<span data-ttu-id="47b45-120">매니페스트 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-120">Manifest reference.</span></span>

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

### <span data-ttu-id="47b45-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="47b45-121">-RegistryName</span></span>
<span data-ttu-id="47b45-122">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="47b45-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="47b45-123">-RepositoryName</span></span>
<span data-ttu-id="47b45-124">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-124">Repository Name.</span></span>

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

### <span data-ttu-id="47b45-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="47b45-125">-Tag</span></span>
<span data-ttu-id="47b45-126">태그.</span><span class="sxs-lookup"><span data-stu-id="47b45-126">Tag.</span></span>

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

### <span data-ttu-id="47b45-127">-확인</span><span class="sxs-lookup"><span data-stu-id="47b45-127">-Confirm</span></span>
<span data-ttu-id="47b45-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b45-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b45-129">-WhatIf</span></span>
<span data-ttu-id="47b45-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b45-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b45-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b45-132">CommonParameters</span></span>
<span data-ttu-id="47b45-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47b45-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b45-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47b45-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b45-135">입력</span><span class="sxs-lookup"><span data-stu-id="47b45-135">INPUTS</span></span>

### <span data-ttu-id="47b45-136">System.String</span><span class="sxs-lookup"><span data-stu-id="47b45-136">System.String</span></span>

## <span data-ttu-id="47b45-137">출력</span><span class="sxs-lookup"><span data-stu-id="47b45-137">OUTPUTS</span></span>

### <span data-ttu-id="47b45-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47b45-138">System.Boolean</span></span>

## <span data-ttu-id="47b45-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47b45-139">NOTES</span></span>

## <span data-ttu-id="47b45-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47b45-140">RELATED LINKS</span></span>
