---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702177"
---
# <span data-ttu-id="526b6-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="526b6-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="526b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="526b6-102">SYNOPSIS</span></span>
<span data-ttu-id="526b6-103">자동화 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="526b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="526b6-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="526b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="526b6-105">DESCRIPTION</span></span>
<span data-ttu-id="526b6-106">**AzureRmAutomationJobOutput** Cmdlet은 Azure Automation 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="526b6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="526b6-107">EXAMPLES</span></span>

### <span data-ttu-id="526b6-108">예제 1: 자동화 작업의 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="526b6-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="526b6-109">이 명령은 지정 된 ID를 갖는 모든 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="526b6-110">변수</span><span class="sxs-lookup"><span data-stu-id="526b6-110">PARAMETERS</span></span>

### <span data-ttu-id="526b6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="526b6-111">-AutomationAccountName</span></span>
<span data-ttu-id="526b6-112">이 cmdlet에서 작업 출력을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526b6-113">-DefaultProfile</span></span>
<span data-ttu-id="526b6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="526b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526b6-115">-Id</span><span class="sxs-lookup"><span data-stu-id="526b6-115">-Id</span></span>
<span data-ttu-id="526b6-116">이 cmdlet이 출력을 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="526b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="526b6-118">이 cmdlet에서 작업 출력을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526b6-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="526b6-119">-StartTime</span></span>
<span data-ttu-id="526b6-120">시작 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="526b6-121">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="526b6-122">Cmdlet은이 시간 후에 만들어진 출력을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526b6-123">-스트림</span><span class="sxs-lookup"><span data-stu-id="526b6-123">-Stream</span></span>
<span data-ttu-id="526b6-124">출력 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-124">Specifies the type of output.</span></span>
<span data-ttu-id="526b6-125">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-125">Valid values are:</span></span> 

- <span data-ttu-id="526b6-126">이상</span><span class="sxs-lookup"><span data-stu-id="526b6-126">Any</span></span>
- <span data-ttu-id="526b6-127">디버깅이</span><span class="sxs-lookup"><span data-stu-id="526b6-127">Debug</span></span>
- <span data-ttu-id="526b6-128">오류</span><span class="sxs-lookup"><span data-stu-id="526b6-128">Error</span></span>
- <span data-ttu-id="526b6-129">결과물</span><span class="sxs-lookup"><span data-stu-id="526b6-129">Output</span></span>
- <span data-ttu-id="526b6-130">진행률과</span><span class="sxs-lookup"><span data-stu-id="526b6-130">Progress</span></span>
- <span data-ttu-id="526b6-131">정보</span><span class="sxs-lookup"><span data-stu-id="526b6-131">Verbose</span></span>
- <span data-ttu-id="526b6-132">오류</span><span class="sxs-lookup"><span data-stu-id="526b6-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526b6-133">CommonParameters</span></span>
<span data-ttu-id="526b6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526b6-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526b6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526b6-136">입력</span><span class="sxs-lookup"><span data-stu-id="526b6-136">INPUTS</span></span>

### <span data-ttu-id="526b6-137">않아야</span><span class="sxs-lookup"><span data-stu-id="526b6-137">None</span></span>
<span data-ttu-id="526b6-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="526b6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="526b6-139">출력</span><span class="sxs-lookup"><span data-stu-id="526b6-139">OUTPUTS</span></span>

### <span data-ttu-id="526b6-140">Microsoft. Azure. JobStream</span><span class="sxs-lookup"><span data-stu-id="526b6-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="526b6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="526b6-141">NOTES</span></span>

## <span data-ttu-id="526b6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="526b6-142">RELATED LINKS</span></span>

[<span data-ttu-id="526b6-143">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="526b6-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="526b6-144">이력서-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="526b6-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="526b6-145">중지-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="526b6-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="526b6-146">일시 중단-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="526b6-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


