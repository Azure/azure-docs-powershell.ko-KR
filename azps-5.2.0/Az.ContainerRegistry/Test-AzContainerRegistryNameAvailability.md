---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347517"
---
# <span data-ttu-id="77ea5-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="77ea5-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="77ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="77ea5-103">컨테이너 레지스트리 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="77ea5-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="77ea5-104">구문</span><span class="sxs-lookup"><span data-stu-id="77ea5-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77ea5-105">설명</span><span class="sxs-lookup"><span data-stu-id="77ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="77ea5-106">이 Test-AzContainerRegistryNameAvailability cmdlet은 컨테이너 레지스트리 이름이 유효하고 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="77ea5-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="77ea5-107">예제</span><span class="sxs-lookup"><span data-stu-id="77ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="77ea5-108">예제 1: 컨테이너 레지스트리 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="77ea5-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="77ea5-109">이 명령은 컨테이너 레지스트리 이름 \` SomeRegistryName의 가용성을 \` 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="77ea5-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="77ea5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77ea5-110">PARAMETERS</span></span>

### <span data-ttu-id="77ea5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ea5-111">-DefaultProfile</span></span>
<span data-ttu-id="77ea5-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="77ea5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77ea5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="77ea5-113">-Name</span></span>
<span data-ttu-id="77ea5-114">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77ea5-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="77ea5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ea5-115">CommonParameters</span></span>
<span data-ttu-id="77ea5-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77ea5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ea5-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77ea5-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ea5-118">입력</span><span class="sxs-lookup"><span data-stu-id="77ea5-118">INPUTS</span></span>

### <span data-ttu-id="77ea5-119">System.String</span><span class="sxs-lookup"><span data-stu-id="77ea5-119">System.String</span></span>

## <span data-ttu-id="77ea5-120">출력</span><span class="sxs-lookup"><span data-stu-id="77ea5-120">OUTPUTS</span></span>

### <span data-ttu-id="77ea5-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="77ea5-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="77ea5-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77ea5-122">NOTES</span></span>

## <span data-ttu-id="77ea5-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77ea5-123">RELATED LINKS</span></span>

[<span data-ttu-id="77ea5-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="77ea5-124">New-AzContainerRegistry</span></span>]()

