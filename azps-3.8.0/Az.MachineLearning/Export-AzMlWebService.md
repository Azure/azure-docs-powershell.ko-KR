---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042789"
---
# <span data-ttu-id="24c12-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="24c12-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="24c12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c12-102">SYNOPSIS</span></span>
<span data-ttu-id="24c12-103">웹 서비스 정의 개체를 JSON 형식의 문자열로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="24c12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24c12-104">SYNTAX</span></span>

### <span data-ttu-id="24c12-105">내보내기 Tofile</span><span class="sxs-lookup"><span data-stu-id="24c12-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c12-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="24c12-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c12-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24c12-107">DESCRIPTION</span></span>
<span data-ttu-id="24c12-108">지정 된 웹 서비스의 정의 개체를 JSON 서식이 지정 된 문자열로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="24c12-109">문자열을 즉시 반환 하거나 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="24c12-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24c12-110">EXAMPLES</span></span>

### <span data-ttu-id="24c12-111">예제 1: 문자열로 내보내기</span><span class="sxs-lookup"><span data-stu-id="24c12-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="24c12-112">예제 2: 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="24c12-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="24c12-113">변수</span><span class="sxs-lookup"><span data-stu-id="24c12-113">PARAMETERS</span></span>

### <span data-ttu-id="24c12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c12-114">-DefaultProfile</span></span>
<span data-ttu-id="24c12-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24c12-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c12-116">-Force</span><span class="sxs-lookup"><span data-stu-id="24c12-116">-Force</span></span>
<span data-ttu-id="24c12-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="24c12-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="24c12-118">-OutputFile</span></span>
<span data-ttu-id="24c12-119">내보낸 정의에 대 한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="24c12-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="24c12-120">-ToJsonString</span></span>
<span data-ttu-id="24c12-121">정의가 JSON 문자열로 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="24c12-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="24c12-122">-WebService</span></span>
<span data-ttu-id="24c12-123">내보낼 웹 서비스 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="24c12-124">-확인</span><span class="sxs-lookup"><span data-stu-id="24c12-124">-Confirm</span></span>
<span data-ttu-id="24c12-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c12-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c12-126">-WhatIf</span></span>
<span data-ttu-id="24c12-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c12-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c12-129">CommonParameters</span></span>
<span data-ttu-id="24c12-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c12-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c12-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c12-132">입력</span><span class="sxs-lookup"><span data-stu-id="24c12-132">INPUTS</span></span>

### <span data-ttu-id="24c12-133">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="24c12-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="24c12-134">출력</span><span class="sxs-lookup"><span data-stu-id="24c12-134">OUTPUTS</span></span>

### <span data-ttu-id="24c12-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24c12-135">System.String</span></span>

## <span data-ttu-id="24c12-136">상속자</span><span class="sxs-lookup"><span data-stu-id="24c12-136">NOTES</span></span>
<span data-ttu-id="24c12-137">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="24c12-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="24c12-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24c12-138">RELATED LINKS</span></span>
