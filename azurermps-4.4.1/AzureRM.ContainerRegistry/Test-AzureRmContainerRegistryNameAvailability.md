---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711606"
---
# <span data-ttu-id="01536-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="01536-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="01536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01536-102">SYNOPSIS</span></span>
<span data-ttu-id="01536-103">컨테이너 레지스트리 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="01536-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01536-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01536-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01536-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01536-105">DESCRIPTION</span></span>
<span data-ttu-id="01536-106">**AzureRmContainerRegistryNameAvailability** cmdlet은 컨테이너 레지스트리 이름이 유효 하며 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="01536-106">The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="01536-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01536-107">EXAMPLES</span></span>

### <span data-ttu-id="01536-108">예제 1: 컨테이너 레지스트리 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="01536-108">Example 1: Check the availability of a container registry name</span></span>
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="01536-109">이 명령은 컨테이너 레지스트리 이름의 사용 가능 여부를 확인 합니다 `SomeRegistryName` .</span><span class="sxs-lookup"><span data-stu-id="01536-109">This command checks the availability of the container registry name `SomeRegistryName`.</span></span>

## <span data-ttu-id="01536-110">변수</span><span class="sxs-lookup"><span data-stu-id="01536-110">PARAMETERS</span></span>

### <span data-ttu-id="01536-111">-이름</span><span class="sxs-lookup"><span data-stu-id="01536-111">-Name</span></span>
<span data-ttu-id="01536-112">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01536-112">Container Registry Name.</span></span>

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

### <span data-ttu-id="01536-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01536-113">-DefaultProfile</span></span>
<span data-ttu-id="01536-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01536-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01536-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01536-115">CommonParameters</span></span>
<span data-ttu-id="01536-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01536-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01536-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01536-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01536-118">입력</span><span class="sxs-lookup"><span data-stu-id="01536-118">INPUTS</span></span>

## <span data-ttu-id="01536-119">출력</span><span class="sxs-lookup"><span data-stu-id="01536-119">OUTPUTS</span></span>

### <span data-ttu-id="01536-120">ContainerRegistry. RegistryNameStatus/.</span><span class="sxs-lookup"><span data-stu-id="01536-120">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="01536-121">상속자</span><span class="sxs-lookup"><span data-stu-id="01536-121">NOTES</span></span>

## <span data-ttu-id="01536-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01536-122">RELATED LINKS</span></span>

[<span data-ttu-id="01536-123">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="01536-123">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

