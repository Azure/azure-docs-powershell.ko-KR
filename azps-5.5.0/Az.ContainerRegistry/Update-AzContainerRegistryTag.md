---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204664"
---
# <span data-ttu-id="c3599-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="c3599-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="c3599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3599-102">SYNOPSIS</span></span>
<span data-ttu-id="c3599-103">ACR 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-103">Update ACR tag.</span></span>

## <span data-ttu-id="c3599-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3599-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3599-105">설명</span><span class="sxs-lookup"><span data-stu-id="c3599-105">DESCRIPTION</span></span>
<span data-ttu-id="c3599-106">ACR 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-106">Update ACR tag.</span></span>
<span data-ttu-id="c3599-107">이 cmdlet을 사용 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="c3599-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="c3599-108">먼저</span><span class="sxs-lookup"><span data-stu-id="c3599-108">first.</span></span>

## <span data-ttu-id="c3599-109">예제</span><span class="sxs-lookup"><span data-stu-id="c3599-109">EXAMPLES</span></span>

### <span data-ttu-id="c3599-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3599-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="c3599-111">레지스트리에서 최신 태그에 대한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="c3599-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3599-112">PARAMETERS</span></span>

### <span data-ttu-id="c3599-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3599-113">-DefaultProfile</span></span>
<span data-ttu-id="c3599-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3599-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="c3599-115">-DeleteEnabled</span></span>
<span data-ttu-id="c3599-116">사용 삭제.</span><span class="sxs-lookup"><span data-stu-id="c3599-116">Delete enable.</span></span>

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

### <span data-ttu-id="c3599-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="c3599-117">-ListEnabled</span></span>
<span data-ttu-id="c3599-118">목록 사용.</span><span class="sxs-lookup"><span data-stu-id="c3599-118">List enable.</span></span>

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

### <span data-ttu-id="c3599-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c3599-119">-Name</span></span>
<span data-ttu-id="c3599-120">태그.</span><span class="sxs-lookup"><span data-stu-id="c3599-120">Tag.</span></span>

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

### <span data-ttu-id="c3599-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="c3599-121">-ReadEnabled</span></span>
<span data-ttu-id="c3599-122">읽기 사용.</span><span class="sxs-lookup"><span data-stu-id="c3599-122">Read enable.</span></span>

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

### <span data-ttu-id="c3599-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c3599-123">-RegistryName</span></span>
<span data-ttu-id="c3599-124">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c3599-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="c3599-125">-RepositoryName</span></span>
<span data-ttu-id="c3599-126">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-126">Repository Name.</span></span>

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

### <span data-ttu-id="c3599-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="c3599-127">-WriteEnabled</span></span>
<span data-ttu-id="c3599-128">쓰기 사용.</span><span class="sxs-lookup"><span data-stu-id="c3599-128">Write enable.</span></span>

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

### <span data-ttu-id="c3599-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3599-129">-Confirm</span></span>
<span data-ttu-id="c3599-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3599-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3599-131">-WhatIf</span></span>
<span data-ttu-id="c3599-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c3599-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3599-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3599-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3599-134">CommonParameters</span></span>
<span data-ttu-id="c3599-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3599-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3599-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3599-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3599-137">입력</span><span class="sxs-lookup"><span data-stu-id="c3599-137">INPUTS</span></span>

### <span data-ttu-id="c3599-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c3599-138">System.String</span></span>

## <span data-ttu-id="c3599-139">출력</span><span class="sxs-lookup"><span data-stu-id="c3599-139">OUTPUTS</span></span>

### <span data-ttu-id="c3599-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="c3599-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="c3599-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3599-141">NOTES</span></span>

## <span data-ttu-id="c3599-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3599-142">RELATED LINKS</span></span>
