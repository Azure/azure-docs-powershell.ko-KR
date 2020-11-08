---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215582"
---
# <span data-ttu-id="c2b02-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="c2b02-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="c2b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b02-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b02-103">Azure 컨테이너 레지스트리의 사용법을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="c2b02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2b02-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2b02-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b02-106">Azure 컨테이너 레지스트리의 사용법을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="c2b02-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c2b02-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b02-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2b02-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="c2b02-109">Azure 컨테이너 레지스트리의 사용법을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="c2b02-110">변수</span><span class="sxs-lookup"><span data-stu-id="c2b02-110">PARAMETERS</span></span>

### <span data-ttu-id="c2b02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b02-111">-DefaultProfile</span></span>
<span data-ttu-id="c2b02-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b02-113">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c2b02-113">-RegistryName</span></span>
<span data-ttu-id="c2b02-114">대상 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b02-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2b02-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b02-117">CommonParameters</span></span>
<span data-ttu-id="c2b02-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b02-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2b02-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b02-120">입력</span><span class="sxs-lookup"><span data-stu-id="c2b02-120">INPUTS</span></span>

### <span data-ttu-id="c2b02-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2b02-121">System.String</span></span>

## <span data-ttu-id="c2b02-122">출력</span><span class="sxs-lookup"><span data-stu-id="c2b02-122">OUTPUTS</span></span>

### <span data-ttu-id="c2b02-123">ContainerRegistry. PSRegistryUsage/.</span><span class="sxs-lookup"><span data-stu-id="c2b02-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="c2b02-124">상속자</span><span class="sxs-lookup"><span data-stu-id="c2b02-124">NOTES</span></span>

## <span data-ttu-id="c2b02-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2b02-125">RELATED LINKS</span></span>
