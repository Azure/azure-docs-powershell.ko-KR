---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 0fad6a81f895643f8783ca8d179d68e31eed6da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976795"
---
# <span data-ttu-id="7e943-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7e943-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="7e943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e943-102">SYNOPSIS</span></span>
<span data-ttu-id="7e943-103">웹 서비스 정의 개체를 JSON 형식의 문자열로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="7e943-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e943-104">SYNTAX</span></span>

### <span data-ttu-id="7e943-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="7e943-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e943-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="7e943-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e943-107">설명</span><span class="sxs-lookup"><span data-stu-id="7e943-107">DESCRIPTION</span></span>
<span data-ttu-id="7e943-108">지정된 웹 서비스의 정의 개체를 JSON 서식이 지정된 문자열로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="7e943-109">문자열을 즉시 반환하거나 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="7e943-110">예제</span><span class="sxs-lookup"><span data-stu-id="7e943-110">EXAMPLES</span></span>

### <span data-ttu-id="7e943-111">예제 1: 문자열로 내보내기</span><span class="sxs-lookup"><span data-stu-id="7e943-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="7e943-112">예제 2: 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="7e943-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="7e943-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e943-113">PARAMETERS</span></span>

### <span data-ttu-id="7e943-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e943-114">-DefaultProfile</span></span>
<span data-ttu-id="7e943-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7e943-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e943-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7e943-116">-Force</span></span>
<span data-ttu-id="7e943-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7e943-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7e943-118">-OutputFile</span></span>
<span data-ttu-id="7e943-119">내보낼 정의에 대한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="7e943-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="7e943-120">-ToJsonString</span></span>
<span data-ttu-id="7e943-121">정의가 JSON 문자열로 내보낼지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="7e943-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="7e943-122">-WebService</span></span>
<span data-ttu-id="7e943-123">내보낼 웹 서비스 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="7e943-124">-확인</span><span class="sxs-lookup"><span data-stu-id="7e943-124">-Confirm</span></span>
<span data-ttu-id="7e943-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e943-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e943-126">-WhatIf</span></span>
<span data-ttu-id="7e943-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e943-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e943-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e943-129">CommonParameters</span></span>
<span data-ttu-id="7e943-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e943-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e943-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7e943-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e943-132">입력</span><span class="sxs-lookup"><span data-stu-id="7e943-132">INPUTS</span></span>

### <span data-ttu-id="7e943-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="7e943-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7e943-134">출력</span><span class="sxs-lookup"><span data-stu-id="7e943-134">OUTPUTS</span></span>

### <span data-ttu-id="7e943-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7e943-135">System.String</span></span>

## <span data-ttu-id="7e943-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e943-136">NOTES</span></span>
<span data-ttu-id="7e943-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="7e943-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7e943-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e943-138">RELATED LINKS</span></span>
