---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: a99d020bbdef81868fb0e4338c7bc6c722723254
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199108"
---
# <span data-ttu-id="d1f63-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="d1f63-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="d1f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f63-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f63-103">ACR에서 리포지토리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="d1f63-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1f63-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1f63-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1f63-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f63-106">ACR에서 리포지토리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="d1f63-107">예제</span><span class="sxs-lookup"><span data-stu-id="d1f63-107">EXAMPLES</span></span>

### <span data-ttu-id="d1f63-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1f63-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="d1f63-109">레지스트리에서 리포지토리 테스트/busybox15를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="d1f63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f63-110">PARAMETERS</span></span>

### <span data-ttu-id="d1f63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f63-111">-DefaultProfile</span></span>
<span data-ttu-id="d1f63-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f63-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f63-113">-Name</span></span>
<span data-ttu-id="d1f63-114">리포지토리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-114">Repository Name.</span></span>

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

### <span data-ttu-id="d1f63-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d1f63-115">-RegistryName</span></span>
<span data-ttu-id="d1f63-116">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="d1f63-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f63-117">-Confirm</span></span>
<span data-ttu-id="d1f63-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f63-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f63-119">-WhatIf</span></span>
<span data-ttu-id="d1f63-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d1f63-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f63-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f63-122">CommonParameters</span></span>
<span data-ttu-id="d1f63-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f63-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1f63-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f63-125">입력</span><span class="sxs-lookup"><span data-stu-id="d1f63-125">INPUTS</span></span>

### <span data-ttu-id="d1f63-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d1f63-126">System.String</span></span>

## <span data-ttu-id="d1f63-127">출력</span><span class="sxs-lookup"><span data-stu-id="d1f63-127">OUTPUTS</span></span>

### <span data-ttu-id="d1f63-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="d1f63-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="d1f63-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1f63-129">NOTES</span></span>

## <span data-ttu-id="d1f63-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1f63-130">RELATED LINKS</span></span>
