---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956336"
---
# <span data-ttu-id="7cd68-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7cd68-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="7cd68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd68-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd68-103">컨테이너 레지스트리 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd68-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="7cd68-104">구문</span><span class="sxs-lookup"><span data-stu-id="7cd68-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cd68-105">설명</span><span class="sxs-lookup"><span data-stu-id="7cd68-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd68-106">Test-AzContainerRegistryNameAvailability cmdlet은 컨테이너 레지스트리 이름이 유효하고 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd68-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="7cd68-107">예제</span><span class="sxs-lookup"><span data-stu-id="7cd68-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd68-108">예제 1: 컨테이너 레지스트리 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="7cd68-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="7cd68-109">이 명령은 컨테이너 레지스트리 이름 \` SomeRegistryName의 가용성을 \` 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd68-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="7cd68-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7cd68-110">PARAMETERS</span></span>

### <span data-ttu-id="7cd68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd68-111">-DefaultProfile</span></span>
<span data-ttu-id="7cd68-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7cd68-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cd68-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7cd68-113">-Name</span></span>
<span data-ttu-id="7cd68-114">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd68-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd68-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd68-115">CommonParameters</span></span>
<span data-ttu-id="7cd68-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd68-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd68-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cd68-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd68-118">입력</span><span class="sxs-lookup"><span data-stu-id="7cd68-118">INPUTS</span></span>

### <span data-ttu-id="7cd68-119">System.String</span><span class="sxs-lookup"><span data-stu-id="7cd68-119">System.String</span></span>

## <span data-ttu-id="7cd68-120">출력</span><span class="sxs-lookup"><span data-stu-id="7cd68-120">OUTPUTS</span></span>

### <span data-ttu-id="7cd68-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="7cd68-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="7cd68-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7cd68-122">NOTES</span></span>

## <span data-ttu-id="7cd68-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cd68-123">RELATED LINKS</span></span>

[<span data-ttu-id="7cd68-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7cd68-124">New-AzContainerRegistry</span></span>]()

