---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: f8923c6f98dad44a56c35cadc4b3e1daedeb1227
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532246"
---
# <span data-ttu-id="a8eb8-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="a8eb8-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="a8eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="a8eb8-103">웹 서비스 정의 개체를 JSON 형식의 문자열로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8eb8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8eb8-104">SYNTAX</span></span>

### <span data-ttu-id="a8eb8-105">파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-105">Export to file.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eb8-106">JSON 문자열로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-106">Export to JSON string.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8eb8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a8eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="a8eb8-108">지정 된 웹 servive의 정의 개체를 JSON 서식이 지정 된 문자열로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="a8eb8-109">문자열을 즉시 반환 하거나 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="a8eb8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a8eb8-110">EXAMPLES</span></span>

### <span data-ttu-id="a8eb8-111">--------------------------예제 1: 문자열로 내보내기--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8eb8-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
<span data-ttu-id="a8eb8-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a8eb8-112">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="a8eb8-113">--------------------------예제 2: 파일로 내보내기--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8eb8-113">--------------------------  Example 2: Export to file  --------------------------</span></span>
<span data-ttu-id="a8eb8-114">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a8eb8-114">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="a8eb8-115">변수</span><span class="sxs-lookup"><span data-stu-id="a8eb8-115">PARAMETERS</span></span>

### <span data-ttu-id="a8eb8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a8eb8-116">-Force</span></span>
<span data-ttu-id="a8eb8-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a8eb8-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a8eb8-118">-OutputFile</span></span>
<span data-ttu-id="a8eb8-119">내보낸 정의에 대 한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb8-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="a8eb8-120">-ToJsonString</span></span>
<span data-ttu-id="a8eb8-121">정의가 JSON 문자열로 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb8-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="a8eb8-122">-WebService</span></span>
<span data-ttu-id="a8eb8-123">내보낼 웹 서비스 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="a8eb8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="a8eb8-124">-Confirm</span></span>
<span data-ttu-id="a8eb8-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8eb8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8eb8-126">-WhatIf</span></span>
<span data-ttu-id="a8eb8-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8eb8-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8eb8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8eb8-129">-DefaultProfile</span></span>
<span data-ttu-id="a8eb8-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8eb8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8eb8-131">CommonParameters</span></span>
<span data-ttu-id="a8eb8-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8eb8-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8eb8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8eb8-134">입력</span><span class="sxs-lookup"><span data-stu-id="a8eb8-134">INPUTS</span></span>

### <span data-ttu-id="a8eb8-135">용</span><span class="sxs-lookup"><span data-stu-id="a8eb8-135">WebService</span></span>
<span data-ttu-id="a8eb8-136">' WebService ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-136">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="a8eb8-137">출력</span><span class="sxs-lookup"><span data-stu-id="a8eb8-137">OUTPUTS</span></span>

### <span data-ttu-id="a8eb8-138">않아야</span><span class="sxs-lookup"><span data-stu-id="a8eb8-138">None</span></span>

## <span data-ttu-id="a8eb8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a8eb8-139">NOTES</span></span>
<span data-ttu-id="a8eb8-140">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="a8eb8-140">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a8eb8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8eb8-141">RELATED LINKS</span></span>

