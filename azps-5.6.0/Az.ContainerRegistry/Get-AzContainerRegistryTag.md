---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990360"
---
# <span data-ttu-id="6d765-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="6d765-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="6d765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d765-102">SYNOPSIS</span></span>
<span data-ttu-id="6d765-103">ACR 태그를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="6d765-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d765-104">SYNTAX</span></span>

### <span data-ttu-id="6d765-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6d765-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d765-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d765-107">설명</span><span class="sxs-lookup"><span data-stu-id="6d765-107">DESCRIPTION</span></span>
<span data-ttu-id="6d765-108">ACR 태그를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-108">Get or list ACR tag.</span></span>
<span data-ttu-id="6d765-109">이 cmdlet을 사용 하시기 바랍니다. `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="6d765-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="6d765-110">먼저.</span><span class="sxs-lookup"><span data-stu-id="6d765-110">first.</span></span>

## <span data-ttu-id="6d765-111">예제</span><span class="sxs-lookup"><span data-stu-id="6d765-111">EXAMPLES</span></span>

### <span data-ttu-id="6d765-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d765-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="6d765-113">레지스트리 아래에 리포지토리 알프스에 대한 태그를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="6d765-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6d765-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="6d765-115">레지스트리 아래 리포지토리 알프스에 대한 태그를 최신으로 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="6d765-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d765-116">PARAMETERS</span></span>

### <span data-ttu-id="6d765-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d765-117">-DefaultProfile</span></span>
<span data-ttu-id="6d765-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d765-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6d765-119">-Name</span></span>
<span data-ttu-id="6d765-120">태그.</span><span class="sxs-lookup"><span data-stu-id="6d765-120">Tag.</span></span>

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

### <span data-ttu-id="6d765-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6d765-121">-RegistryName</span></span>
<span data-ttu-id="6d765-122">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="6d765-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="6d765-123">-RepositoryName</span></span>
<span data-ttu-id="6d765-124">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-124">Repository Name.</span></span>

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

### <span data-ttu-id="6d765-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d765-125">CommonParameters</span></span>
<span data-ttu-id="6d765-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d765-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d765-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d765-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d765-128">입력</span><span class="sxs-lookup"><span data-stu-id="6d765-128">INPUTS</span></span>

### <span data-ttu-id="6d765-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6d765-129">System.String</span></span>

## <span data-ttu-id="6d765-130">출력</span><span class="sxs-lookup"><span data-stu-id="6d765-130">OUTPUTS</span></span>

### <span data-ttu-id="6d765-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="6d765-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="6d765-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="6d765-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="6d765-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d765-133">NOTES</span></span>

## <span data-ttu-id="6d765-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d765-134">RELATED LINKS</span></span>
