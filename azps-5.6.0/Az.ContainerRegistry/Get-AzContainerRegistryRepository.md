---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990397"
---
# <span data-ttu-id="e4a47-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="e4a47-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="e4a47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4a47-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a47-103">ACR 리포지토리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="e4a47-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4a47-104">SYNTAX</span></span>

### <span data-ttu-id="e4a47-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e4a47-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4a47-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4a47-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4a47-107">설명</span><span class="sxs-lookup"><span data-stu-id="e4a47-107">DESCRIPTION</span></span>
<span data-ttu-id="e4a47-108">ACR 리포지토리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="e4a47-109">목록은 리포지토리 이름만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-109">List returns repository names only.</span></span>

## <span data-ttu-id="e4a47-110">예제</span><span class="sxs-lookup"><span data-stu-id="e4a47-110">EXAMPLES</span></span>

### <span data-ttu-id="e4a47-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4a47-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="e4a47-112">레지스트리에 모든 리포지토리를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-112">List all repositories in registry.</span></span>

### <span data-ttu-id="e4a47-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e4a47-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="e4a47-114">레지스트리에 처음 3개 리포지토리를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="e4a47-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e4a47-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="e4a47-116">레지스트리에서 리포지토리 알프스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="e4a47-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4a47-117">PARAMETERS</span></span>

### <span data-ttu-id="e4a47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a47-118">-DefaultProfile</span></span>
<span data-ttu-id="e4a47-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4a47-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e4a47-120">-Name</span></span>
<span data-ttu-id="e4a47-121">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-121">Repository Name.</span></span>

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

### <span data-ttu-id="e4a47-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e4a47-122">-RegistryName</span></span>
<span data-ttu-id="e4a47-123">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="e4a47-124">-First</span><span class="sxs-lookup"><span data-stu-id="e4a47-124">-First</span></span>
<span data-ttu-id="e4a47-125">첫 번째 n 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a47-126">CommonParameters</span></span>
<span data-ttu-id="e4a47-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4a47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a47-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4a47-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a47-129">입력</span><span class="sxs-lookup"><span data-stu-id="e4a47-129">INPUTS</span></span>

### <span data-ttu-id="e4a47-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e4a47-130">System.String</span></span>

## <span data-ttu-id="e4a47-131">출력</span><span class="sxs-lookup"><span data-stu-id="e4a47-131">OUTPUTS</span></span>

### <span data-ttu-id="e4a47-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e4a47-132">System.String</span></span>

### <span data-ttu-id="e4a47-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="e4a47-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="e4a47-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4a47-134">NOTES</span></span>

## <span data-ttu-id="e4a47-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4a47-135">RELATED LINKS</span></span>
