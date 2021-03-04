---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: 45572cbd2255a604e492c7740d1749a0ad968845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956283"
---
# <span data-ttu-id="89756-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="89756-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="89756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89756-102">SYNOPSIS</span></span>
<span data-ttu-id="89756-103">ACR 리포지토리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89756-103">Update ACR repository.</span></span>

## <span data-ttu-id="89756-104">구문</span><span class="sxs-lookup"><span data-stu-id="89756-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89756-105">설명</span><span class="sxs-lookup"><span data-stu-id="89756-105">DESCRIPTION</span></span>
<span data-ttu-id="89756-106">ACR 리포지토리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89756-106">Update ACR repository.</span></span>

## <span data-ttu-id="89756-107">예제</span><span class="sxs-lookup"><span data-stu-id="89756-107">EXAMPLES</span></span>

### <span data-ttu-id="89756-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="89756-108">Example 1</span></span>
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

<span data-ttu-id="89756-109">레지스트리 아래 리포지토리 알프스에 대한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89756-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="89756-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="89756-110">PARAMETERS</span></span>

### <span data-ttu-id="89756-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89756-111">-DefaultProfile</span></span>
<span data-ttu-id="89756-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89756-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89756-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="89756-113">-DeleteEnabled</span></span>
<span data-ttu-id="89756-114">사용 안 을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="89756-114">Delete enable.</span></span>

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

### <span data-ttu-id="89756-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="89756-115">-ListEnabled</span></span>
<span data-ttu-id="89756-116">목록 사용.</span><span class="sxs-lookup"><span data-stu-id="89756-116">List enable.</span></span>

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

### <span data-ttu-id="89756-117">-Name</span><span class="sxs-lookup"><span data-stu-id="89756-117">-Name</span></span>
<span data-ttu-id="89756-118">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89756-118">Repository Name.</span></span>

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

### <span data-ttu-id="89756-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="89756-119">-ReadEnabled</span></span>
<span data-ttu-id="89756-120">읽기 사용.</span><span class="sxs-lookup"><span data-stu-id="89756-120">Read enable.</span></span>

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

### <span data-ttu-id="89756-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="89756-121">-RegistryName</span></span>
<span data-ttu-id="89756-122">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89756-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="89756-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="89756-123">-WriteEnabled</span></span>
<span data-ttu-id="89756-124">쓰기 사용.</span><span class="sxs-lookup"><span data-stu-id="89756-124">Write enable.</span></span>

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

### <span data-ttu-id="89756-125">-확인</span><span class="sxs-lookup"><span data-stu-id="89756-125">-Confirm</span></span>
<span data-ttu-id="89756-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="89756-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89756-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89756-127">-WhatIf</span></span>
<span data-ttu-id="89756-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="89756-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89756-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89756-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89756-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89756-130">CommonParameters</span></span>
<span data-ttu-id="89756-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89756-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89756-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89756-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89756-133">입력</span><span class="sxs-lookup"><span data-stu-id="89756-133">INPUTS</span></span>

### <span data-ttu-id="89756-134">System.String</span><span class="sxs-lookup"><span data-stu-id="89756-134">System.String</span></span>

## <span data-ttu-id="89756-135">출력</span><span class="sxs-lookup"><span data-stu-id="89756-135">OUTPUTS</span></span>

### <span data-ttu-id="89756-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="89756-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="89756-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89756-137">NOTES</span></span>

## <span data-ttu-id="89756-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89756-138">RELATED LINKS</span></span>
