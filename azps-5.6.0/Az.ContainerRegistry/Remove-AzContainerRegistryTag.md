---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956416"
---
# <span data-ttu-id="c9528-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="c9528-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="c9528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9528-102">SYNOPSIS</span></span>
<span data-ttu-id="c9528-103">ACR 태그를 언태그합니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-103">Untag ACR tag.</span></span>

## <span data-ttu-id="c9528-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9528-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9528-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9528-105">DESCRIPTION</span></span>
<span data-ttu-id="c9528-106">ACR 태그를 언태그합니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-106">Untag ACR tag.</span></span>
<span data-ttu-id="c9528-107">이 cmdlet을 사용 하시기 바랍니다. `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="c9528-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="c9528-108">먼저.</span><span class="sxs-lookup"><span data-stu-id="c9528-108">first.</span></span>

## <span data-ttu-id="c9528-109">예제</span><span class="sxs-lookup"><span data-stu-id="c9528-109">EXAMPLES</span></span>

### <span data-ttu-id="c9528-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9528-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="c9528-111">레지스트리 아래에서 alpine:tag 태그를 태그 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="c9528-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c9528-112">PARAMETERS</span></span>

### <span data-ttu-id="c9528-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9528-113">-DefaultProfile</span></span>
<span data-ttu-id="c9528-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9528-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c9528-115">-Name</span></span>
<span data-ttu-id="c9528-116">태그.</span><span class="sxs-lookup"><span data-stu-id="c9528-116">Tag.</span></span>

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

### <span data-ttu-id="c9528-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c9528-117">-RegistryName</span></span>
<span data-ttu-id="c9528-118">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c9528-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="c9528-119">-RepositoryName</span></span>
<span data-ttu-id="c9528-120">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-120">Repository Name.</span></span>

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

### <span data-ttu-id="c9528-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c9528-121">-Confirm</span></span>
<span data-ttu-id="c9528-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9528-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9528-123">-WhatIf</span></span>
<span data-ttu-id="c9528-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9528-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9528-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9528-126">CommonParameters</span></span>
<span data-ttu-id="c9528-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9528-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9528-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9528-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9528-129">입력</span><span class="sxs-lookup"><span data-stu-id="c9528-129">INPUTS</span></span>

### <span data-ttu-id="c9528-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c9528-130">System.String</span></span>

## <span data-ttu-id="c9528-131">출력</span><span class="sxs-lookup"><span data-stu-id="c9528-131">OUTPUTS</span></span>

### <span data-ttu-id="c9528-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9528-132">System.Boolean</span></span>

## <span data-ttu-id="c9528-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9528-133">NOTES</span></span>

## <span data-ttu-id="c9528-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9528-134">RELATED LINKS</span></span>
