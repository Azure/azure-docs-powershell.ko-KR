---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3858c2ad6ca90716d5c9140949a683b9c409a105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015355"
---
# <span data-ttu-id="42f54-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42f54-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="42f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f54-102">SYNOPSIS</span></span>
<span data-ttu-id="42f54-103">작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-103">Cancels a job.</span></span>

## <span data-ttu-id="42f54-104">구문</span><span class="sxs-lookup"><span data-stu-id="42f54-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f54-105">설명</span><span class="sxs-lookup"><span data-stu-id="42f54-105">DESCRIPTION</span></span>
<span data-ttu-id="42f54-106">**Stop-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="42f54-107">예제</span><span class="sxs-lookup"><span data-stu-id="42f54-107">EXAMPLES</span></span>

### <span data-ttu-id="42f54-108">예제 1: 작업 취소</span><span class="sxs-lookup"><span data-stu-id="42f54-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="42f54-109">이 명령은 지정된 ID로 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="42f54-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42f54-110">PARAMETERS</span></span>

### <span data-ttu-id="42f54-111">-Account</span><span class="sxs-lookup"><span data-stu-id="42f54-111">-Account</span></span>
<span data-ttu-id="42f54-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="42f54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f54-113">-DefaultProfile</span></span>
<span data-ttu-id="42f54-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="42f54-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42f54-115">-Force</span><span class="sxs-lookup"><span data-stu-id="42f54-115">-Force</span></span>
<span data-ttu-id="42f54-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42f54-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="42f54-117">-JobId</span></span>
<span data-ttu-id="42f54-118">취소할 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="42f54-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42f54-119">-PassThru</span></span>
<span data-ttu-id="42f54-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42f54-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42f54-122">-확인</span><span class="sxs-lookup"><span data-stu-id="42f54-122">-Confirm</span></span>
<span data-ttu-id="42f54-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f54-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f54-124">-WhatIf</span></span>
<span data-ttu-id="42f54-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f54-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f54-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f54-127">CommonParameters</span></span>
<span data-ttu-id="42f54-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42f54-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f54-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="42f54-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f54-130">입력</span><span class="sxs-lookup"><span data-stu-id="42f54-130">INPUTS</span></span>

### <span data-ttu-id="42f54-131">System.String</span><span class="sxs-lookup"><span data-stu-id="42f54-131">System.String</span></span>

### <span data-ttu-id="42f54-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="42f54-132">System.Guid</span></span>

### <span data-ttu-id="42f54-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42f54-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42f54-134">출력</span><span class="sxs-lookup"><span data-stu-id="42f54-134">OUTPUTS</span></span>

### <span data-ttu-id="42f54-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42f54-135">System.Boolean</span></span>

## <span data-ttu-id="42f54-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42f54-136">NOTES</span></span>

## <span data-ttu-id="42f54-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42f54-137">RELATED LINKS</span></span>

[<span data-ttu-id="42f54-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42f54-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="42f54-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42f54-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="42f54-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="42f54-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


