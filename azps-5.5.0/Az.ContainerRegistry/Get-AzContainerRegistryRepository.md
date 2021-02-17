---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: 7da65515138ff6afa97e6c05f9baa764d6ab920c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196913"
---
# <span data-ttu-id="56113-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="56113-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="56113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56113-102">SYNOPSIS</span></span>
<span data-ttu-id="56113-103">ACR 리포지토리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="56113-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="56113-104">구문</span><span class="sxs-lookup"><span data-stu-id="56113-104">SYNTAX</span></span>

### <span data-ttu-id="56113-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="56113-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56113-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="56113-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56113-107">설명</span><span class="sxs-lookup"><span data-stu-id="56113-107">DESCRIPTION</span></span>
<span data-ttu-id="56113-108">ACR 리포지토리를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="56113-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="56113-109">목록은 리포지토리 이름만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="56113-109">List returns repository names only.</span></span>

## <span data-ttu-id="56113-110">예제</span><span class="sxs-lookup"><span data-stu-id="56113-110">EXAMPLES</span></span>

### <span data-ttu-id="56113-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="56113-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="56113-112">레지스트리의 모든 리포지토리를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="56113-112">List all repositories in registry.</span></span>

### <span data-ttu-id="56113-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="56113-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="56113-114">레지스트리에 처음 3개 리포지토리를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="56113-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="56113-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="56113-115">Example 3</span></span>
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

<span data-ttu-id="56113-116">레지스트리에서 리포지토리 알프스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56113-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="56113-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56113-117">PARAMETERS</span></span>

### <span data-ttu-id="56113-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56113-118">-DefaultProfile</span></span>
<span data-ttu-id="56113-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56113-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56113-120">-Name</span><span class="sxs-lookup"><span data-stu-id="56113-120">-Name</span></span>
<span data-ttu-id="56113-121">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56113-121">Repository Name.</span></span>

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

### <span data-ttu-id="56113-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="56113-122">-RegistryName</span></span>
<span data-ttu-id="56113-123">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56113-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="56113-124">-First</span><span class="sxs-lookup"><span data-stu-id="56113-124">-First</span></span>
<span data-ttu-id="56113-125">첫 번째 n개 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="56113-125">First n results.</span></span>

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

### <span data-ttu-id="56113-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56113-126">CommonParameters</span></span>
<span data-ttu-id="56113-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56113-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56113-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56113-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56113-129">입력</span><span class="sxs-lookup"><span data-stu-id="56113-129">INPUTS</span></span>

### <span data-ttu-id="56113-130">System.String</span><span class="sxs-lookup"><span data-stu-id="56113-130">System.String</span></span>

## <span data-ttu-id="56113-131">출력</span><span class="sxs-lookup"><span data-stu-id="56113-131">OUTPUTS</span></span>

### <span data-ttu-id="56113-132">System.String</span><span class="sxs-lookup"><span data-stu-id="56113-132">System.String</span></span>

### <span data-ttu-id="56113-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="56113-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="56113-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56113-134">NOTES</span></span>

## <span data-ttu-id="56113-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56113-135">RELATED LINKS</span></span>
