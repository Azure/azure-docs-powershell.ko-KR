---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 030f0b00ba77bc967a53ce43c4f08d66c214f67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956288"
---
# <span data-ttu-id="ade21-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="ade21-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="ade21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade21-102">SYNOPSIS</span></span>
<span data-ttu-id="ade21-103">ACR 매니페스트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="ade21-104">구문</span><span class="sxs-lookup"><span data-stu-id="ade21-104">SYNTAX</span></span>

### <span data-ttu-id="ade21-105">ByManifestParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ade21-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade21-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade21-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ade21-107">설명</span><span class="sxs-lookup"><span data-stu-id="ade21-107">DESCRIPTION</span></span>
<span data-ttu-id="ade21-108">ACR 매니페스트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-108">Update ACR manifest.</span></span>
<span data-ttu-id="ade21-109">이 cmdlet을 사용 하시기 바랍니다. `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="ade21-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="ade21-110">먼저.</span><span class="sxs-lookup"><span data-stu-id="ade21-110">first.</span></span>

## <span data-ttu-id="ade21-111">예제</span><span class="sxs-lookup"><span data-stu-id="ade21-111">EXAMPLES</span></span>

### <span data-ttu-id="ade21-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ade21-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="ade21-113">매니페스트 sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 아래에서 특성 업데이트</span><span class="sxs-lookup"><span data-stu-id="ade21-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="ade21-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ade21-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="ade21-115">레지스트리 아래 태그를 사용하여 매니페스트에 대한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="ade21-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ade21-116">PARAMETERS</span></span>

### <span data-ttu-id="ade21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade21-117">-DefaultProfile</span></span>
<span data-ttu-id="ade21-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade21-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="ade21-119">-DeleteEnabled</span></span>
<span data-ttu-id="ade21-120">사용 안 을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-120">Delete enable.</span></span>

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

### <span data-ttu-id="ade21-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="ade21-121">-ListEnabled</span></span>
<span data-ttu-id="ade21-122">목록 사용.</span><span class="sxs-lookup"><span data-stu-id="ade21-122">List enable.</span></span>

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

### <span data-ttu-id="ade21-123">-매니페스트</span><span class="sxs-lookup"><span data-stu-id="ade21-123">-Manifest</span></span>
<span data-ttu-id="ade21-124">매니페스트 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-124">Manifest reference.</span></span>

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

### <span data-ttu-id="ade21-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="ade21-125">-ReadEnabled</span></span>
<span data-ttu-id="ade21-126">읽기 사용.</span><span class="sxs-lookup"><span data-stu-id="ade21-126">Read enable.</span></span>

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

### <span data-ttu-id="ade21-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ade21-127">-RegistryName</span></span>
<span data-ttu-id="ade21-128">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="ade21-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="ade21-129">-RepositoryName</span></span>
<span data-ttu-id="ade21-130">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-130">Repository Name.</span></span>

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

### <span data-ttu-id="ade21-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ade21-131">-Tag</span></span>
<span data-ttu-id="ade21-132">태그.</span><span class="sxs-lookup"><span data-stu-id="ade21-132">Tag.</span></span>

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

### <span data-ttu-id="ade21-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="ade21-133">-WriteEnabled</span></span>
<span data-ttu-id="ade21-134">쓰기 사용.</span><span class="sxs-lookup"><span data-stu-id="ade21-134">Write enable.</span></span>

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

### <span data-ttu-id="ade21-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ade21-135">-Confirm</span></span>
<span data-ttu-id="ade21-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade21-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade21-137">-WhatIf</span></span>
<span data-ttu-id="ade21-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade21-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade21-140">CommonParameters</span></span>
<span data-ttu-id="ade21-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ade21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade21-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade21-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade21-143">입력</span><span class="sxs-lookup"><span data-stu-id="ade21-143">INPUTS</span></span>

### <span data-ttu-id="ade21-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ade21-144">System.String</span></span>

## <span data-ttu-id="ade21-145">출력</span><span class="sxs-lookup"><span data-stu-id="ade21-145">OUTPUTS</span></span>

### <span data-ttu-id="ade21-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="ade21-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="ade21-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ade21-147">NOTES</span></span>

## <span data-ttu-id="ade21-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ade21-148">RELATED LINKS</span></span>
