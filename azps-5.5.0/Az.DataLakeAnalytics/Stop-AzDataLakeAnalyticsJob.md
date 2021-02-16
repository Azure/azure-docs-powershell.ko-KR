---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194737"
---
# <span data-ttu-id="df5d9-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="df5d9-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="df5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="df5d9-103">작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-103">Cancels a job.</span></span>

## <span data-ttu-id="df5d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="df5d9-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df5d9-105">설명</span><span class="sxs-lookup"><span data-stu-id="df5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="df5d9-106">**Stop-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="df5d9-107">예제</span><span class="sxs-lookup"><span data-stu-id="df5d9-107">EXAMPLES</span></span>

### <span data-ttu-id="df5d9-108">예제 1: 작업 취소</span><span class="sxs-lookup"><span data-stu-id="df5d9-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="df5d9-109">이 명령은 지정된 ID로 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="df5d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df5d9-110">PARAMETERS</span></span>

### <span data-ttu-id="df5d9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="df5d9-111">-Account</span></span>
<span data-ttu-id="df5d9-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df5d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5d9-113">-DefaultProfile</span></span>
<span data-ttu-id="df5d9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="df5d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df5d9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="df5d9-115">-Force</span></span>
<span data-ttu-id="df5d9-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df5d9-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="df5d9-117">-JobId</span></span>
<span data-ttu-id="df5d9-118">취소할 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df5d9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df5d9-119">-PassThru</span></span>
<span data-ttu-id="df5d9-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df5d9-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5d9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df5d9-122">-Confirm</span></span>
<span data-ttu-id="df5d9-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5d9-124">-WhatIf</span></span>
<span data-ttu-id="df5d9-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df5d9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df5d9-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df5d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5d9-127">CommonParameters</span></span>
<span data-ttu-id="df5d9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df5d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5d9-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df5d9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5d9-130">입력</span><span class="sxs-lookup"><span data-stu-id="df5d9-130">INPUTS</span></span>

### <span data-ttu-id="df5d9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="df5d9-131">System.String</span></span>

### <span data-ttu-id="df5d9-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="df5d9-132">System.Guid</span></span>

### <span data-ttu-id="df5d9-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df5d9-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df5d9-134">출력</span><span class="sxs-lookup"><span data-stu-id="df5d9-134">OUTPUTS</span></span>

### <span data-ttu-id="df5d9-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df5d9-135">System.Boolean</span></span>

## <span data-ttu-id="df5d9-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df5d9-136">NOTES</span></span>

## <span data-ttu-id="df5d9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df5d9-137">RELATED LINKS</span></span>

[<span data-ttu-id="df5d9-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="df5d9-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="df5d9-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="df5d9-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="df5d9-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="df5d9-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


