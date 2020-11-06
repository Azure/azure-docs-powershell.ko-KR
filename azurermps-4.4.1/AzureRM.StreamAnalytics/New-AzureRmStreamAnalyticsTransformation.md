---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: eb9f8b82e8ff8a0f60931953f2a3b4349e7b4a4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529058"
---
# <span data-ttu-id="ae441-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ae441-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="ae441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae441-102">SYNOPSIS</span></span>
<span data-ttu-id="ae441-103">작업 내에서 변환을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae441-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae441-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae441-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae441-105">DESCRIPTION</span></span>
<span data-ttu-id="ae441-106">**AzureRmStreamAnalyticsTransformation** Cmdlet은 Stream Analytics 작업 내에서 변환을 만들거나 기존 변환을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="ae441-107">변환의 이름은에 지정 될 수 있습니다. JSON 파일 또는 명령줄</span><span class="sxs-lookup"><span data-stu-id="ae441-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="ae441-108">둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="ae441-109">이미 존재 하 고 Force 매개 변수를 지정 하지 않은 변환을 지정 하는 경우 cmdlet은 기존 변환을 바꿀지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="ae441-110">*Force* 매개 변수를 지정 하 고 기존 변형 이름을 지정 하면 확인 없이 변환이 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="ae441-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ae441-111">EXAMPLES</span></span>

### <span data-ttu-id="ae441-112">예제 1: 작업에서 변형 만들기 또는 바꾸기</span><span class="sxs-lookup"><span data-stu-id="ae441-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="ae441-113">이 명령은 StreamingJob 이라는 작업에서 StreamingJobTransform 이라는 변환을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="ae441-114">기존 변환이 해당 이름으로 이미 정의 되어 있으면 cmdlet에서 해당 이름을 바꿀지 여부를 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ae441-115">예제 2: 작업에서 변형 바꾸기</span><span class="sxs-lookup"><span data-stu-id="ae441-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="ae441-116">이 명령은 확인 없이 job StreamingJob의 StreamingJobTransform 정의를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="ae441-117">변수</span><span class="sxs-lookup"><span data-stu-id="ae441-117">PARAMETERS</span></span>

### <span data-ttu-id="ae441-118">-파일</span><span class="sxs-lookup"><span data-stu-id="ae441-118">-File</span></span>
<span data-ttu-id="ae441-119">만들 Azure Stream Analytics 변환의 JSON 표시를 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae441-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ae441-120">-Force</span></span>
<span data-ttu-id="ae441-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae441-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="ae441-122">-JobName</span></span>
<span data-ttu-id="ae441-123">Azure Stream Analytics 변환을 만들 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae441-124">-이름</span><span class="sxs-lookup"><span data-stu-id="ae441-124">-Name</span></span>
<span data-ttu-id="ae441-125">만들 Azure Stream Analytics 변환의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-125">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae441-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae441-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae441-127">Azure Stream Analytics 변환을 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-127">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae441-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ae441-128">-Confirm</span></span>
<span data-ttu-id="ae441-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae441-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae441-130">-WhatIf</span></span>
<span data-ttu-id="ae441-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae441-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae441-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae441-133">-DefaultProfile</span></span>
<span data-ttu-id="ae441-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae441-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae441-135">CommonParameters</span></span>
<span data-ttu-id="ae441-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae441-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae441-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae441-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae441-138">입력</span><span class="sxs-lookup"><span data-stu-id="ae441-138">INPUTS</span></span>

## <span data-ttu-id="ae441-139">출력</span><span class="sxs-lookup"><span data-stu-id="ae441-139">OUTPUTS</span></span>

### <span data-ttu-id="ae441-140">PSTransformation를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="ae441-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="ae441-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ae441-141">NOTES</span></span>

## <span data-ttu-id="ae441-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae441-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae441-143">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ae441-143">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)


