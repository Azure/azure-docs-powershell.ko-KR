---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711538"
---
# <span data-ttu-id="ef512-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="ef512-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="ef512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef512-102">SYNOPSIS</span></span>
<span data-ttu-id="ef512-103">JSON 개체를 웹 서비스 정의로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef512-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef512-104">SYNTAX</span></span>

### <span data-ttu-id="ef512-105">JSON 파일에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-105">Import from JSON file.</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef512-106">JSON 문자열에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-106">Import from JSON string.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef512-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ef512-107">DESCRIPTION</span></span>
<span data-ttu-id="ef512-108">직접 또는 참조 되는 파일에 지정 된 Import-AzureRmMlWebService cmdlet 가져오기 및 New-AzureRmMlWebService cmdlet에 전달할 수 있는 웹 서비스 정의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="ef512-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ef512-109">EXAMPLES</span></span>

### <span data-ttu-id="ef512-110">--------------------------예제 1: 문자열--------------------------가져오기</span><span class="sxs-lookup"><span data-stu-id="ef512-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
<span data-ttu-id="ef512-111">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ef512-111">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="ef512-112">--------------------------예제 2: 파일 경로에서 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef512-112">--------------------------  Example 2: Import from file path  --------------------------</span></span>
<span data-ttu-id="ef512-113">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ef512-113">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="ef512-114">변수</span><span class="sxs-lookup"><span data-stu-id="ef512-114">PARAMETERS</span></span>

### <span data-ttu-id="ef512-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ef512-115">-InputFile</span></span>
<span data-ttu-id="ef512-116">가져올 웹 서비스 정의를 포함 하는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef512-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="ef512-117">-JsonString</span></span>
<span data-ttu-id="ef512-118">가져올 웹 서비스 정의가 포함 된 JSON 형식 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef512-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef512-119">-DefaultProfile</span></span>
<span data-ttu-id="ef512-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef512-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef512-121">CommonParameters</span></span>
<span data-ttu-id="ef512-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef512-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef512-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef512-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef512-124">입력</span><span class="sxs-lookup"><span data-stu-id="ef512-124">INPUTS</span></span>

## <span data-ttu-id="ef512-125">출력</span><span class="sxs-lookup"><span data-stu-id="ef512-125">OUTPUTS</span></span>

### <span data-ttu-id="ef512-126">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="ef512-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ef512-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ef512-127">NOTES</span></span>
<span data-ttu-id="ef512-128">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="ef512-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ef512-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef512-129">RELATED LINKS</span></span>

