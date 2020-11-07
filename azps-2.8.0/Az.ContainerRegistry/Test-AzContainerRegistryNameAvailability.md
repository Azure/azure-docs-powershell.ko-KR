---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 114fd947cb69f14e0e67b8a48cbe8b26a7c34101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697114"
---
# <span data-ttu-id="8a65f-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8a65f-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="8a65f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a65f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a65f-103">컨테이너 레지스트리 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a65f-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="8a65f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a65f-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a65f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a65f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a65f-106">Test-AzContainerRegistryNameAvailability cmdlet은 컨테이너 레지스트리 이름이 유효 하며 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a65f-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="8a65f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a65f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a65f-108">예제 1: 컨테이너 레지스트리 이름의 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="8a65f-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="8a65f-109">이 명령은 컨테이너 레지스트리 이름 SomeRegistryName의 사용 가능 여부를 확인 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="8a65f-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="8a65f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a65f-110">PARAMETERS</span></span>

### <span data-ttu-id="8a65f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a65f-111">-DefaultProfile</span></span>
<span data-ttu-id="8a65f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8a65f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a65f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="8a65f-113">-Name</span></span>
<span data-ttu-id="8a65f-114">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a65f-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="8a65f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a65f-115">CommonParameters</span></span>
<span data-ttu-id="8a65f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a65f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a65f-117">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a65f-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a65f-118">입력</span><span class="sxs-lookup"><span data-stu-id="8a65f-118">INPUTS</span></span>

### <span data-ttu-id="8a65f-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a65f-119">System.String</span></span>

## <span data-ttu-id="8a65f-120">출력</span><span class="sxs-lookup"><span data-stu-id="8a65f-120">OUTPUTS</span></span>

### <span data-ttu-id="8a65f-121">ContainerRegistry. RegistryNameStatus/.</span><span class="sxs-lookup"><span data-stu-id="8a65f-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="8a65f-122">상속자</span><span class="sxs-lookup"><span data-stu-id="8a65f-122">NOTES</span></span>

## <span data-ttu-id="8a65f-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a65f-123">RELATED LINKS</span></span>

[<span data-ttu-id="8a65f-124">새로운 AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a65f-124">New-AzContainerRegistry</span></span>]()
