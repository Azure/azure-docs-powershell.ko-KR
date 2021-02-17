---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 85623106a932ba9419da0c07cc4bcb6c52e5e838
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177329"
---
# <span data-ttu-id="deb64-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="deb64-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="deb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb64-102">SYNOPSIS</span></span>
<span data-ttu-id="deb64-103">ACR 매니페스트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="deb64-104">구문</span><span class="sxs-lookup"><span data-stu-id="deb64-104">SYNTAX</span></span>

### <span data-ttu-id="deb64-105">ByManifestParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="deb64-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb64-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="deb64-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb64-107">설명</span><span class="sxs-lookup"><span data-stu-id="deb64-107">DESCRIPTION</span></span>
<span data-ttu-id="deb64-108">ACR 매니페스트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-108">Update ACR manifest.</span></span>
<span data-ttu-id="deb64-109">이 cmdlet을 사용 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="deb64-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="deb64-110">먼저</span><span class="sxs-lookup"><span data-stu-id="deb64-110">first.</span></span>

## <span data-ttu-id="deb64-111">예제</span><span class="sxs-lookup"><span data-stu-id="deb64-111">EXAMPLES</span></span>

### <span data-ttu-id="deb64-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="deb64-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="deb64-113">레지스트리에서 매니페스트 sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321에 대한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="deb64-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="deb64-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="deb64-115">레지스트리에서 최신 태그로 매니페스트에 대한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="deb64-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deb64-116">PARAMETERS</span></span>

### <span data-ttu-id="deb64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb64-117">-DefaultProfile</span></span>
<span data-ttu-id="deb64-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb64-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="deb64-119">-DeleteEnabled</span></span>
<span data-ttu-id="deb64-120">삭제 사용.</span><span class="sxs-lookup"><span data-stu-id="deb64-120">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb64-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="deb64-121">-ListEnabled</span></span>
<span data-ttu-id="deb64-122">목록 사용.</span><span class="sxs-lookup"><span data-stu-id="deb64-122">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb64-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="deb64-123">-Manifest</span></span>
<span data-ttu-id="deb64-124">매니페스트 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-124">Manifest reference.</span></span>

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

### <span data-ttu-id="deb64-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="deb64-125">-ReadEnabled</span></span>
<span data-ttu-id="deb64-126">읽기 사용.</span><span class="sxs-lookup"><span data-stu-id="deb64-126">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb64-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="deb64-127">-RegistryName</span></span>
<span data-ttu-id="deb64-128">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="deb64-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="deb64-129">-RepositoryName</span></span>
<span data-ttu-id="deb64-130">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-130">Repository Name.</span></span>

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

### <span data-ttu-id="deb64-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="deb64-131">-Tag</span></span>
<span data-ttu-id="deb64-132">태그.</span><span class="sxs-lookup"><span data-stu-id="deb64-132">Tag.</span></span>

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

### <span data-ttu-id="deb64-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="deb64-133">-WriteEnabled</span></span>
<span data-ttu-id="deb64-134">쓰기 사용.</span><span class="sxs-lookup"><span data-stu-id="deb64-134">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb64-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="deb64-135">-Confirm</span></span>
<span data-ttu-id="deb64-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb64-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb64-137">-WhatIf</span></span>
<span data-ttu-id="deb64-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="deb64-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb64-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb64-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb64-140">CommonParameters</span></span>
<span data-ttu-id="deb64-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="deb64-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb64-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="deb64-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb64-143">입력</span><span class="sxs-lookup"><span data-stu-id="deb64-143">INPUTS</span></span>

### <span data-ttu-id="deb64-144">System.String</span><span class="sxs-lookup"><span data-stu-id="deb64-144">System.String</span></span>

## <span data-ttu-id="deb64-145">출력</span><span class="sxs-lookup"><span data-stu-id="deb64-145">OUTPUTS</span></span>

### <span data-ttu-id="deb64-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="deb64-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="deb64-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="deb64-147">NOTES</span></span>

## <span data-ttu-id="deb64-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="deb64-148">RELATED LINKS</span></span>
