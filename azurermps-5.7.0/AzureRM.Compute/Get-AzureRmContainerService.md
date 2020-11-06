---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531110"
---
# <span data-ttu-id="a2e81-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a2e81-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="a2e81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e81-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e81-103">컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2e81-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a2e81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2e81-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e81-106">**Get-AzureRmContainerService** cmdlet은 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="a2e81-107">상태, 마스터 및 에이전트 수, 마스터 및 에이전트의 정규화 된 도메인 이름 등 컨테이너 서비스의 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="a2e81-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a2e81-108">EXAMPLES</span></span>

### <span data-ttu-id="a2e81-109">예제 1: 컨테이너 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="a2e81-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a2e81-110">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a2e81-111">변수</span><span class="sxs-lookup"><span data-stu-id="a2e81-111">PARAMETERS</span></span>

### <span data-ttu-id="a2e81-112">-이름</span><span class="sxs-lookup"><span data-stu-id="a2e81-112">-Name</span></span>
<span data-ttu-id="a2e81-113">이 cmdlet이 가져오는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e81-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e81-114">-ResourceGroupName</span></span>
<span data-ttu-id="a2e81-115">이 cmdlet이 가져오는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e81-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e81-116">CommonParameters</span></span>
<span data-ttu-id="a2e81-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e81-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e81-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e81-119">입력</span><span class="sxs-lookup"><span data-stu-id="a2e81-119">INPUTS</span></span>

### <span data-ttu-id="a2e81-120">않아야</span><span class="sxs-lookup"><span data-stu-id="a2e81-120">None</span></span>
<span data-ttu-id="a2e81-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2e81-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2e81-122">출력</span><span class="sxs-lookup"><span data-stu-id="a2e81-122">OUTPUTS</span></span>

## <span data-ttu-id="a2e81-123">상속자</span><span class="sxs-lookup"><span data-stu-id="a2e81-123">NOTES</span></span>

## <span data-ttu-id="a2e81-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2e81-124">RELATED LINKS</span></span>

[<span data-ttu-id="a2e81-125">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a2e81-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="a2e81-126">제거-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a2e81-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="a2e81-127">업데이트-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a2e81-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


