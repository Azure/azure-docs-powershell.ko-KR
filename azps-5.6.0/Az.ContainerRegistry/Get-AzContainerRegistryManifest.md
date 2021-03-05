---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004416"
---
# <span data-ttu-id="606d8-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="606d8-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="606d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606d8-102">SYNOPSIS</span></span>
<span data-ttu-id="606d8-103">ACR 매니페스트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="606d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="606d8-104">SYNTAX</span></span>

### <span data-ttu-id="606d8-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="606d8-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="606d8-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="606d8-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="606d8-107">설명</span><span class="sxs-lookup"><span data-stu-id="606d8-107">DESCRIPTION</span></span>
<span data-ttu-id="606d8-108">ACR 매니페스트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="606d8-109">이 cmdlet을 사용 하시기 바랍니다. `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="606d8-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="606d8-110">먼저.</span><span class="sxs-lookup"><span data-stu-id="606d8-110">first.</span></span>

## <span data-ttu-id="606d8-111">예제</span><span class="sxs-lookup"><span data-stu-id="606d8-111">EXAMPLES</span></span>

### <span data-ttu-id="606d8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="606d8-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="606d8-113">레지스트리 아래 리포지토리 알프스에 대한 매니페스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="606d8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="606d8-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="606d8-115">매니페스트 sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0</span><span class="sxs-lookup"><span data-stu-id="606d8-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="606d8-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="606d8-116">PARAMETERS</span></span>

### <span data-ttu-id="606d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606d8-117">-DefaultProfile</span></span>
<span data-ttu-id="606d8-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="606d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="606d8-119">-Name</span></span>
<span data-ttu-id="606d8-120">매니페스트 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606d8-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="606d8-121">-RegistryName</span></span>
<span data-ttu-id="606d8-122">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="606d8-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="606d8-123">-RepositoryName</span></span>
<span data-ttu-id="606d8-124">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-124">Repository Name.</span></span>

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

### <span data-ttu-id="606d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606d8-125">CommonParameters</span></span>
<span data-ttu-id="606d8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="606d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606d8-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="606d8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606d8-128">입력</span><span class="sxs-lookup"><span data-stu-id="606d8-128">INPUTS</span></span>

### <span data-ttu-id="606d8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="606d8-129">System.String</span></span>

## <span data-ttu-id="606d8-130">출력</span><span class="sxs-lookup"><span data-stu-id="606d8-130">OUTPUTS</span></span>

### <span data-ttu-id="606d8-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="606d8-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="606d8-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="606d8-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="606d8-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="606d8-133">NOTES</span></span>

## <span data-ttu-id="606d8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="606d8-134">RELATED LINKS</span></span>
