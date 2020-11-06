---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: d38971c15c46cbeaba6e9dda87ad0f3b7febbfd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533187"
---
# <span data-ttu-id="a13fe-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a13fe-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="a13fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a13fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a13fe-103">자동화 DSC 컴파일 작업의 로깅 스트림을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a13fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a13fe-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a13fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a13fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a13fe-106">**AzureRmAutomationDscCompilationJobOutput** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 컴파일 작업의 스트림 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="a13fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a13fe-107">EXAMPLES</span></span>

### <span data-ttu-id="a13fe-108">예제 1: DSC 컴파일 작업의 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="a13fe-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="a13fe-109">첫 번째 명령은 Get-AzureRmAutomationDscCompilationJob cmdlet을 사용 하 여 Contoso17 이라는 Automation 계정의 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="a13fe-110">명령이 $Jobs 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="a13fe-111">두 번째 명령은 $Jobs 배열의 첫 번째 구성원에 대 한 모든 스트림에 대 한 컴파일 작업 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="a13fe-112">변수</span><span class="sxs-lookup"><span data-stu-id="a13fe-112">PARAMETERS</span></span>

### <span data-ttu-id="a13fe-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a13fe-113">-AutomationAccountName</span></span>
<span data-ttu-id="a13fe-114">DSC 컴파일 작업을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="a13fe-115">-Id</span><span class="sxs-lookup"><span data-stu-id="a13fe-115">-Id</span></span>
<span data-ttu-id="a13fe-116">이 cmdlet이 출력을 가져오는 DSC 컴파일 작업의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-116">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="a13fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a13fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="a13fe-118">이 cmdlet이 스트림 레코드를 가져오는 DSC 컴파일 작업을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-118">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="a13fe-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a13fe-119">-StartTime</span></span>
<span data-ttu-id="a13fe-120">시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-120">Specifies a start time.</span></span>
<span data-ttu-id="a13fe-121">이 cmdlet은 DSC 컴파일 작업이이 시간 후에 출력 하는 스트림 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-121">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="a13fe-122">-스트림</span><span class="sxs-lookup"><span data-stu-id="a13fe-122">-Stream</span></span>
<span data-ttu-id="a13fe-123">이 cmdlet이 가져오는 출력의 스트림 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-123">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="a13fe-124">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-124">Valid values are:</span></span> 

- <span data-ttu-id="a13fe-125">이상</span><span class="sxs-lookup"><span data-stu-id="a13fe-125">Any</span></span> 
- <span data-ttu-id="a13fe-126">오류</span><span class="sxs-lookup"><span data-stu-id="a13fe-126">Warning</span></span> 
- <span data-ttu-id="a13fe-127">오류</span><span class="sxs-lookup"><span data-stu-id="a13fe-127">Error</span></span> 
- <span data-ttu-id="a13fe-128">정보</span><span class="sxs-lookup"><span data-stu-id="a13fe-128">Verbose</span></span>

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

### <span data-ttu-id="a13fe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13fe-129">-DefaultProfile</span></span>
<span data-ttu-id="a13fe-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a13fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13fe-131">CommonParameters</span></span>
<span data-ttu-id="a13fe-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a13fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13fe-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a13fe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13fe-134">입력</span><span class="sxs-lookup"><span data-stu-id="a13fe-134">INPUTS</span></span>

## <span data-ttu-id="a13fe-135">출력</span><span class="sxs-lookup"><span data-stu-id="a13fe-135">OUTPUTS</span></span>

### <span data-ttu-id="a13fe-136">Microsoft. Azure. JobStream</span><span class="sxs-lookup"><span data-stu-id="a13fe-136">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="a13fe-137">상속자</span><span class="sxs-lookup"><span data-stu-id="a13fe-137">NOTES</span></span>

## <span data-ttu-id="a13fe-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a13fe-138">RELATED LINKS</span></span>

[<span data-ttu-id="a13fe-139">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a13fe-139">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="a13fe-140">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a13fe-140">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


