---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495511"
---
# <span data-ttu-id="6b586-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b586-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="6b586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b586-102">SYNOPSIS</span></span>
<span data-ttu-id="6b586-103">작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-103">Cancels a job.</span></span>

## <span data-ttu-id="6b586-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b586-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b586-105">설명</span><span class="sxs-lookup"><span data-stu-id="6b586-105">DESCRIPTION</span></span>
<span data-ttu-id="6b586-106">**Stop-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="6b586-107">예제</span><span class="sxs-lookup"><span data-stu-id="6b586-107">EXAMPLES</span></span>

### <span data-ttu-id="6b586-108">예제 1: 작업 취소</span><span class="sxs-lookup"><span data-stu-id="6b586-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="6b586-109">이 명령은 지정된 ID로 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="6b586-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b586-110">PARAMETERS</span></span>

### <span data-ttu-id="6b586-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6b586-111">-Account</span></span>
<span data-ttu-id="6b586-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6b586-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b586-113">-DefaultProfile</span></span>
<span data-ttu-id="6b586-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6b586-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b586-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6b586-115">-Force</span></span>
<span data-ttu-id="6b586-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b586-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b586-117">-JobId</span></span>
<span data-ttu-id="6b586-118">취소할 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="6b586-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b586-119">-PassThru</span></span>
<span data-ttu-id="6b586-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6b586-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b586-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b586-122">-Confirm</span></span>
<span data-ttu-id="6b586-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b586-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b586-124">-WhatIf</span></span>
<span data-ttu-id="6b586-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6b586-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b586-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b586-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b586-127">CommonParameters</span></span>
<span data-ttu-id="6b586-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b586-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b586-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6b586-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b586-130">입력</span><span class="sxs-lookup"><span data-stu-id="6b586-130">INPUTS</span></span>

### <span data-ttu-id="6b586-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6b586-131">System.String</span></span>

### <span data-ttu-id="6b586-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6b586-132">System.Guid</span></span>

### <span data-ttu-id="6b586-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b586-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b586-134">출력</span><span class="sxs-lookup"><span data-stu-id="6b586-134">OUTPUTS</span></span>

### <span data-ttu-id="6b586-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b586-135">System.Boolean</span></span>

## <span data-ttu-id="6b586-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b586-136">NOTES</span></span>

## <span data-ttu-id="6b586-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b586-137">RELATED LINKS</span></span>

[<span data-ttu-id="6b586-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b586-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="6b586-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b586-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="6b586-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6b586-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


