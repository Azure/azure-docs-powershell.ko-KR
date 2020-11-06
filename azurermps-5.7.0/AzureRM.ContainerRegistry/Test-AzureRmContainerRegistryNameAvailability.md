---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531071"
---
# <span data-ttu-id="bb7bc-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bb7bc-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="bb7bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7bc-103">컨테이너 레지스트리 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7bc-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb7bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb7bc-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb7bc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb7bc-105">DESCRIPTION</span></span>
<span data-ttu-id="bb7bc-106">Test-AzureRmContainerRegistryNameAvailability cmdlet은 컨테이너 레지스트리 이름이 유효 하며 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7bc-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="bb7bc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb7bc-107">EXAMPLES</span></span>

### <span data-ttu-id="bb7bc-108">예제 1: 컨테이너 레지스트리 이름의 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="bb7bc-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="bb7bc-109">이 명령은 컨테이너 레지스트리 이름 SomeRegistryName의 사용 가능 여부를 확인 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="bb7bc-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="bb7bc-110">변수</span><span class="sxs-lookup"><span data-stu-id="bb7bc-110">PARAMETERS</span></span>

### <span data-ttu-id="bb7bc-111">-이름</span><span class="sxs-lookup"><span data-stu-id="bb7bc-111">-Name</span></span>
<span data-ttu-id="bb7bc-112">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb7bc-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7bc-113">-DefaultProfile</span></span>
<span data-ttu-id="bb7bc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bb7bc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7bc-115">CommonParameters</span></span>
<span data-ttu-id="bb7bc-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7bc-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb7bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7bc-118">입력</span><span class="sxs-lookup"><span data-stu-id="bb7bc-118">INPUTS</span></span>

### <span data-ttu-id="bb7bc-119">않아야</span><span class="sxs-lookup"><span data-stu-id="bb7bc-119">None</span></span>
<span data-ttu-id="bb7bc-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb7bc-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb7bc-121">출력</span><span class="sxs-lookup"><span data-stu-id="bb7bc-121">OUTPUTS</span></span>

### <span data-ttu-id="bb7bc-122">ContainerRegistry. RegistryNameStatus/.</span><span class="sxs-lookup"><span data-stu-id="bb7bc-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="bb7bc-123">상속자</span><span class="sxs-lookup"><span data-stu-id="bb7bc-123">NOTES</span></span>

## <span data-ttu-id="bb7bc-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb7bc-124">RELATED LINKS</span></span>

[<span data-ttu-id="bb7bc-125">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bb7bc-125">New-AzureRmContainerRegistry</span></span>]()

