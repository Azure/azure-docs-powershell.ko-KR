---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: ce6f235669ebe4a32958229422f4612f3b8cb340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196884"
---
# <span data-ttu-id="f26d8-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="f26d8-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="f26d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f26d8-103">ACR 리포지토리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-103">Update ACR repository.</span></span>

## <span data-ttu-id="f26d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f26d8-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f26d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="f26d8-105">DESCRIPTION</span></span>
<span data-ttu-id="f26d8-106">ACR 리포지토리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-106">Update ACR repository.</span></span>

## <span data-ttu-id="f26d8-107">예제</span><span class="sxs-lookup"><span data-stu-id="f26d8-107">EXAMPLES</span></span>

### <span data-ttu-id="f26d8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f26d8-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="f26d8-109">레지스트리에서 리포지토리 알프스에 대한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="f26d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f26d8-110">PARAMETERS</span></span>

### <span data-ttu-id="f26d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26d8-111">-DefaultProfile</span></span>
<span data-ttu-id="f26d8-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f26d8-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="f26d8-113">-DeleteEnabled</span></span>
<span data-ttu-id="f26d8-114">사용 삭제.</span><span class="sxs-lookup"><span data-stu-id="f26d8-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d8-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="f26d8-115">-ListEnabled</span></span>
<span data-ttu-id="f26d8-116">목록 사용.</span><span class="sxs-lookup"><span data-stu-id="f26d8-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f26d8-117">-Name</span></span>
<span data-ttu-id="f26d8-118">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-118">Repository Name.</span></span>

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

### <span data-ttu-id="f26d8-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="f26d8-119">-ReadEnabled</span></span>
<span data-ttu-id="f26d8-120">읽기 사용.</span><span class="sxs-lookup"><span data-stu-id="f26d8-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d8-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f26d8-121">-RegistryName</span></span>
<span data-ttu-id="f26d8-122">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="f26d8-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="f26d8-123">-WriteEnabled</span></span>
<span data-ttu-id="f26d8-124">쓰기 사용.</span><span class="sxs-lookup"><span data-stu-id="f26d8-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f26d8-125">-Confirm</span></span>
<span data-ttu-id="f26d8-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f26d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f26d8-127">-WhatIf</span></span>
<span data-ttu-id="f26d8-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f26d8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f26d8-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f26d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26d8-130">CommonParameters</span></span>
<span data-ttu-id="f26d8-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26d8-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f26d8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26d8-133">입력</span><span class="sxs-lookup"><span data-stu-id="f26d8-133">INPUTS</span></span>

### <span data-ttu-id="f26d8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f26d8-134">System.String</span></span>

## <span data-ttu-id="f26d8-135">출력</span><span class="sxs-lookup"><span data-stu-id="f26d8-135">OUTPUTS</span></span>

### <span data-ttu-id="f26d8-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="f26d8-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="f26d8-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f26d8-137">NOTES</span></span>

## <span data-ttu-id="f26d8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f26d8-138">RELATED LINKS</span></span>
