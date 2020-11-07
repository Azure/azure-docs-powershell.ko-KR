---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 7a39d010759228e15dd5aee36788f9373ab879bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701632"
---
# <span data-ttu-id="017ad-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="017ad-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="017ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="017ad-102">SYNOPSIS</span></span>
<span data-ttu-id="017ad-103">자동화 DSC 컴파일 작업의 로깅 스트림을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="017ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="017ad-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="017ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="017ad-105">DESCRIPTION</span></span>
<span data-ttu-id="017ad-106">**AzAutomationDscCompilationJobOutput** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 컴파일 작업의 스트림 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="017ad-107">예제의</span><span class="sxs-lookup"><span data-stu-id="017ad-107">EXAMPLES</span></span>

### <span data-ttu-id="017ad-108">예제 1: DSC 컴파일 작업의 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="017ad-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="017ad-109">첫 번째 명령은 Get-AzAutomationDscCompilationJob cmdlet을 사용 하 여 Contoso17 이라는 Automation 계정의 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="017ad-110">명령이 $Jobs 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="017ad-111">두 번째 명령은 $Jobs 배열의 첫 번째 구성원에 대 한 모든 스트림에 대 한 컴파일 작업 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="017ad-112">변수</span><span class="sxs-lookup"><span data-stu-id="017ad-112">PARAMETERS</span></span>

### <span data-ttu-id="017ad-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="017ad-113">-AutomationAccountName</span></span>
<span data-ttu-id="017ad-114">DSC 컴파일 작업을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="017ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017ad-115">-DefaultProfile</span></span>
<span data-ttu-id="017ad-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="017ad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="017ad-117">-Id</span><span class="sxs-lookup"><span data-stu-id="017ad-117">-Id</span></span>
<span data-ttu-id="017ad-118">이 cmdlet이 출력을 가져오는 DSC 컴파일 작업의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="017ad-120">이 cmdlet이 스트림 레코드를 가져오는 DSC 컴파일 작업을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="017ad-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="017ad-121">-StartTime</span></span>
<span data-ttu-id="017ad-122">시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-122">Specifies a start time.</span></span>
<span data-ttu-id="017ad-123">이 cmdlet은 DSC 컴파일 작업이이 시간 후에 출력 하는 스트림 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017ad-124">-스트림</span><span class="sxs-lookup"><span data-stu-id="017ad-124">-Stream</span></span>
<span data-ttu-id="017ad-125">이 cmdlet이 가져오는 출력의 스트림 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="017ad-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-126">Valid values are:</span></span> 
- <span data-ttu-id="017ad-127">이상</span><span class="sxs-lookup"><span data-stu-id="017ad-127">Any</span></span> 
- <span data-ttu-id="017ad-128">오류</span><span class="sxs-lookup"><span data-stu-id="017ad-128">Warning</span></span> 
- <span data-ttu-id="017ad-129">오류</span><span class="sxs-lookup"><span data-stu-id="017ad-129">Error</span></span> 
- <span data-ttu-id="017ad-130">정보</span><span class="sxs-lookup"><span data-stu-id="017ad-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="017ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017ad-131">CommonParameters</span></span>
<span data-ttu-id="017ad-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="017ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017ad-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="017ad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017ad-134">입력</span><span class="sxs-lookup"><span data-stu-id="017ad-134">INPUTS</span></span>

### <span data-ttu-id="017ad-135">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="017ad-135">System.Guid</span></span>

### <span data-ttu-id="017ad-136">CompilationJobStreamType-. m m.</span><span class="sxs-lookup"><span data-stu-id="017ad-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="017ad-137">시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="017ad-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="017ad-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="017ad-138">System.String</span></span>

## <span data-ttu-id="017ad-139">출력</span><span class="sxs-lookup"><span data-stu-id="017ad-139">OUTPUTS</span></span>

### <span data-ttu-id="017ad-140">Microsoft. Azure. JobStream</span><span class="sxs-lookup"><span data-stu-id="017ad-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="017ad-141">상속자</span><span class="sxs-lookup"><span data-stu-id="017ad-141">NOTES</span></span>

## <span data-ttu-id="017ad-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="017ad-142">RELATED LINKS</span></span>

[<span data-ttu-id="017ad-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="017ad-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="017ad-144">시작-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="017ad-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


