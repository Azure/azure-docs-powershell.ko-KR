---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877722"
---
# <span data-ttu-id="2dca2-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="2dca2-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="2dca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dca2-102">SYNOPSIS</span></span>
<span data-ttu-id="2dca2-103">JSON 개체를 웹 서비스 정의로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2dca2-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="2dca2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dca2-104">SYNTAX</span></span>

### <span data-ttu-id="2dca2-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="2dca2-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dca2-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="2dca2-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dca2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2dca2-107">DESCRIPTION</span></span>
<span data-ttu-id="2dca2-108">직접 또는 참조 되는 파일에 지정 된 Import-AzMlWebService cmdlet 가져오기 및 New-AzMlWebService cmdlet에 전달할 수 있는 웹 서비스 정의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dca2-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="2dca2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2dca2-109">EXAMPLES</span></span>

### <span data-ttu-id="2dca2-110">예제 1: 문자열에서 가져오기</span><span class="sxs-lookup"><span data-stu-id="2dca2-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="2dca2-111">예제 2: 파일 경로에서 가져오기</span><span class="sxs-lookup"><span data-stu-id="2dca2-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="2dca2-112">변수</span><span class="sxs-lookup"><span data-stu-id="2dca2-112">PARAMETERS</span></span>

### <span data-ttu-id="2dca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dca2-113">-DefaultProfile</span></span>
<span data-ttu-id="2dca2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2dca2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dca2-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2dca2-115">-InputFile</span></span>
<span data-ttu-id="2dca2-116">가져올 웹 서비스 정의를 포함 하는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2dca2-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dca2-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="2dca2-117">-JsonString</span></span>
<span data-ttu-id="2dca2-118">가져올 웹 서비스 정의가 포함 된 JSON 형식 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2dca2-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dca2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dca2-119">CommonParameters</span></span>
<span data-ttu-id="2dca2-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dca2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dca2-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dca2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dca2-122">입력</span><span class="sxs-lookup"><span data-stu-id="2dca2-122">INPUTS</span></span>

### <span data-ttu-id="2dca2-123">않아야</span><span class="sxs-lookup"><span data-stu-id="2dca2-123">None</span></span>

## <span data-ttu-id="2dca2-124">출력</span><span class="sxs-lookup"><span data-stu-id="2dca2-124">OUTPUTS</span></span>

### <span data-ttu-id="2dca2-125">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="2dca2-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2dca2-126">상속자</span><span class="sxs-lookup"><span data-stu-id="2dca2-126">NOTES</span></span>
<span data-ttu-id="2dca2-127">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="2dca2-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2dca2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dca2-128">RELATED LINKS</span></span>
