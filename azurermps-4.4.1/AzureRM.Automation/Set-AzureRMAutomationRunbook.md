---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528328"
---
# <span data-ttu-id="8b8ac-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="8b8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8ac-103">Runbook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b8ac-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b8ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="8b8ac-106">**AzureRmAutomationRunbook** CMDLET은 APS에서 Azure 자동화 runbook의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="8b8ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b8ac-107">EXAMPLES</span></span>

### <span data-ttu-id="8b8ac-108">예제 1: runbook에 대 한 자세한 로깅 설정</span><span class="sxs-lookup"><span data-stu-id="8b8ac-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8b8ac-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 지정 된 runbook의 작업에 대 한 자세한 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8b8ac-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b8ac-110">PARAMETERS</span></span>

### <span data-ttu-id="8b8ac-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b8ac-111">-AutomationAccountName</span></span>
<span data-ttu-id="8b8ac-112">이 cmdlet이 runbook을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="8b8ac-113">-설명</span><span class="sxs-lookup"><span data-stu-id="8b8ac-113">-Description</span></span>
<span data-ttu-id="8b8ac-114">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-114">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8ac-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="8b8ac-115">-LogProgress</span></span>
<span data-ttu-id="8b8ac-116">Runbook이 진행률을 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-116">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8ac-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="8b8ac-117">-LogVerbose</span></span>
<span data-ttu-id="8b8ac-118">로깅에 자세한 정보가 포함 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-118">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8ac-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8b8ac-119">-Name</span></span>
<span data-ttu-id="8b8ac-120">이 cmdlet이 수정 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b8ac-122">이 cmdlet이 runbook을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="8b8ac-123">태그</span><span class="sxs-lookup"><span data-stu-id="8b8ac-123">-Tags</span></span>
<span data-ttu-id="8b8ac-124">수정 된 runbook의 현재 태그를 바꿀 태그 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8ac-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8ac-125">-DefaultProfile</span></span>
<span data-ttu-id="8b8ac-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b8ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8ac-127">CommonParameters</span></span>
<span data-ttu-id="8b8ac-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b8ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8ac-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8ac-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8ac-130">입력</span><span class="sxs-lookup"><span data-stu-id="8b8ac-130">INPUTS</span></span>

## <span data-ttu-id="8b8ac-131">출력</span><span class="sxs-lookup"><span data-stu-id="8b8ac-131">OUTPUTS</span></span>

### <span data-ttu-id="8b8ac-132">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="8b8ac-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8b8ac-133">NOTES</span></span>

## <span data-ttu-id="8b8ac-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b8ac-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b8ac-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-137">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-138">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-139">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-140">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-141">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="8b8ac-142">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8b8ac-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


