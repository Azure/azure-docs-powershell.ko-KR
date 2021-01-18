---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494345"
---
# <span data-ttu-id="6d9e2-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="6d9e2-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="6d9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9e2-103">Automation DSC 컴파일 작업의 로깅 스트림을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="6d9e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d9e2-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="6d9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9e2-106">**Get-AzAutomationDscCompilationJobOutput** cmdlet은 Azure Automation에서 APS DSC(Desired State Configuration) 컴파일 작업의 스트림 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="6d9e2-107">예제</span><span class="sxs-lookup"><span data-stu-id="6d9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="6d9e2-108">예제 1: DSC 컴파일 작업의 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="6d9e2-109">첫 번째 명령은 Get-AzAutomationDscCompilationJob cmdlet을 사용하여 Contoso17이라는 Automation 계정에서 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="6d9e2-110">이 명령은 해당 개체를 $Jobs 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="6d9e2-111">두 번째 명령은 $Jobs 배열의 첫 번째 멤버에 대한 모든 스트림에 대한 컴파일 작업 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="6d9e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9e2-112">PARAMETERS</span></span>

### <span data-ttu-id="6d9e2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6d9e2-113">-AutomationAccountName</span></span>
<span data-ttu-id="6d9e2-114">DSC 컴파일 작업을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="6d9e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9e2-115">-DefaultProfile</span></span>
<span data-ttu-id="6d9e2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6d9e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d9e2-117">-Id</span><span class="sxs-lookup"><span data-stu-id="6d9e2-117">-Id</span></span>
<span data-ttu-id="6d9e2-118">이 cmdlet이 출력을 얻을 DSC 컴파일 작업의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="6d9e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d9e2-120">이 cmdlet이 스트림 레코드를 얻을 DSC 컴파일 작업을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="6d9e2-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6d9e2-121">-StartTime</span></span>
<span data-ttu-id="6d9e2-122">시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-122">Specifies a start time.</span></span>
<span data-ttu-id="6d9e2-123">이 cmdlet은 이 시간 후에 DSC 컴파일 작업이 출력하는 스트림 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="6d9e2-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="6d9e2-124">-Stream</span></span>
<span data-ttu-id="6d9e2-125">이 cmdlet에서 얻을 출력에 대한 스트림 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="6d9e2-126">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="6d9e2-126">Valid values are:</span></span> 
- <span data-ttu-id="6d9e2-127">모든</span><span class="sxs-lookup"><span data-stu-id="6d9e2-127">Any</span></span> 
- <span data-ttu-id="6d9e2-128">경고</span><span class="sxs-lookup"><span data-stu-id="6d9e2-128">Warning</span></span> 
- <span data-ttu-id="6d9e2-129">오류</span><span class="sxs-lookup"><span data-stu-id="6d9e2-129">Error</span></span> 
- <span data-ttu-id="6d9e2-130">Verbose</span><span class="sxs-lookup"><span data-stu-id="6d9e2-130">Verbose</span></span>

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

### <span data-ttu-id="6d9e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9e2-131">CommonParameters</span></span>
<span data-ttu-id="6d9e2-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9e2-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d9e2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9e2-134">입력</span><span class="sxs-lookup"><span data-stu-id="6d9e2-134">INPUTS</span></span>

### <span data-ttu-id="6d9e2-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6d9e2-135">System.Guid</span></span>

### <span data-ttu-id="6d9e2-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="6d9e2-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="6d9e2-137">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d9e2-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6d9e2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6d9e2-138">System.String</span></span>

## <span data-ttu-id="6d9e2-139">출력</span><span class="sxs-lookup"><span data-stu-id="6d9e2-139">OUTPUTS</span></span>

### <span data-ttu-id="6d9e2-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="6d9e2-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="6d9e2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d9e2-141">NOTES</span></span>

## <span data-ttu-id="6d9e2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d9e2-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d9e2-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6d9e2-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="6d9e2-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6d9e2-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


