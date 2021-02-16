---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199097"
---
# <span data-ttu-id="7a12e-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="7a12e-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="7a12e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a12e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a12e-103">ACR 태그 태그를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-103">Untag ACR tag.</span></span>

## <span data-ttu-id="7a12e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a12e-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a12e-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a12e-105">DESCRIPTION</span></span>
<span data-ttu-id="7a12e-106">ACR 태그 태그를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-106">Untag ACR tag.</span></span>
<span data-ttu-id="7a12e-107">이 cmdlet을 사용 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="7a12e-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="7a12e-108">먼저</span><span class="sxs-lookup"><span data-stu-id="7a12e-108">first.</span></span>

## <span data-ttu-id="7a12e-109">예제</span><span class="sxs-lookup"><span data-stu-id="7a12e-109">EXAMPLES</span></span>

### <span data-ttu-id="7a12e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a12e-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="7a12e-111">레지스트리에서 alpine:tag 태그 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="7a12e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a12e-112">PARAMETERS</span></span>

### <span data-ttu-id="7a12e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a12e-113">-DefaultProfile</span></span>
<span data-ttu-id="7a12e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a12e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7a12e-115">-Name</span></span>
<span data-ttu-id="7a12e-116">태그.</span><span class="sxs-lookup"><span data-stu-id="7a12e-116">Tag.</span></span>

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

### <span data-ttu-id="7a12e-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7a12e-117">-RegistryName</span></span>
<span data-ttu-id="7a12e-118">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="7a12e-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="7a12e-119">-RepositoryName</span></span>
<span data-ttu-id="7a12e-120">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-120">Repository Name.</span></span>

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

### <span data-ttu-id="7a12e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a12e-121">-Confirm</span></span>
<span data-ttu-id="7a12e-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a12e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a12e-123">-WhatIf</span></span>
<span data-ttu-id="7a12e-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a12e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a12e-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a12e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a12e-126">CommonParameters</span></span>
<span data-ttu-id="7a12e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a12e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a12e-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a12e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a12e-129">입력</span><span class="sxs-lookup"><span data-stu-id="7a12e-129">INPUTS</span></span>

### <span data-ttu-id="7a12e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7a12e-130">System.String</span></span>

## <span data-ttu-id="7a12e-131">출력</span><span class="sxs-lookup"><span data-stu-id="7a12e-131">OUTPUTS</span></span>

### <span data-ttu-id="7a12e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a12e-132">System.Boolean</span></span>

## <span data-ttu-id="7a12e-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a12e-133">NOTES</span></span>

## <span data-ttu-id="7a12e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a12e-134">RELATED LINKS</span></span>
