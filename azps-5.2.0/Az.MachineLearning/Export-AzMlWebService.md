---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343569"
---
# <span data-ttu-id="9947b-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="9947b-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="9947b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9947b-102">SYNOPSIS</span></span>
<span data-ttu-id="9947b-103">웹 서비스 정의 개체를 JSON 형식 문자열로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="9947b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9947b-104">SYNTAX</span></span>

### <span data-ttu-id="9947b-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="9947b-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9947b-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="9947b-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9947b-107">설명</span><span class="sxs-lookup"><span data-stu-id="9947b-107">DESCRIPTION</span></span>
<span data-ttu-id="9947b-108">지정된 웹 서비스에 대한 정의 개체를 JSON 형식 문자열로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="9947b-109">문자열을 즉시 반환하거나 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="9947b-110">예제</span><span class="sxs-lookup"><span data-stu-id="9947b-110">EXAMPLES</span></span>

### <span data-ttu-id="9947b-111">예제 1: 문자열로 내보내기</span><span class="sxs-lookup"><span data-stu-id="9947b-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="9947b-112">예제 2: 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="9947b-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="9947b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9947b-113">PARAMETERS</span></span>

### <span data-ttu-id="9947b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9947b-114">-DefaultProfile</span></span>
<span data-ttu-id="9947b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9947b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9947b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9947b-116">-Force</span></span>
<span data-ttu-id="9947b-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9947b-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9947b-118">-OutputFile</span></span>
<span data-ttu-id="9947b-119">내보낼 정의에 대한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9947b-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="9947b-120">-ToJsonString</span></span>
<span data-ttu-id="9947b-121">정의를 JSON 문자열로 내보낼지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9947b-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="9947b-122">-WebService</span></span>
<span data-ttu-id="9947b-123">내보낼 웹 서비스 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9947b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9947b-124">-Confirm</span></span>
<span data-ttu-id="9947b-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9947b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9947b-126">-WhatIf</span></span>
<span data-ttu-id="9947b-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9947b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9947b-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9947b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9947b-129">CommonParameters</span></span>
<span data-ttu-id="9947b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9947b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9947b-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9947b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9947b-132">입력</span><span class="sxs-lookup"><span data-stu-id="9947b-132">INPUTS</span></span>

### <span data-ttu-id="9947b-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="9947b-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="9947b-134">출력</span><span class="sxs-lookup"><span data-stu-id="9947b-134">OUTPUTS</span></span>

### <span data-ttu-id="9947b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9947b-135">System.String</span></span>

## <span data-ttu-id="9947b-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9947b-136">NOTES</span></span>
<span data-ttu-id="9947b-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="9947b-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9947b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9947b-138">RELATED LINKS</span></span>
