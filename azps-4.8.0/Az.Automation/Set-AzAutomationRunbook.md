---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048509"
---
# <span data-ttu-id="5c79b-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="5c79b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c79b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c79b-103">Runbook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-103">Modifies a runbook.</span></span>

## <span data-ttu-id="5c79b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c79b-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c79b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c79b-105">DESCRIPTION</span></span>
<span data-ttu-id="5c79b-106">**AzAutomationRunbook** CMDLET은 APS에서 Azure 자동화 runbook의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="5c79b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5c79b-107">EXAMPLES</span></span>

### <span data-ttu-id="5c79b-108">예제 1: runbook에 대 한 자세한 로깅 설정</span><span class="sxs-lookup"><span data-stu-id="5c79b-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5c79b-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 지정 된 runbook의 작업에 대 한 자세한 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5c79b-110">변수</span><span class="sxs-lookup"><span data-stu-id="5c79b-110">PARAMETERS</span></span>

### <span data-ttu-id="5c79b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5c79b-111">-AutomationAccountName</span></span>
<span data-ttu-id="5c79b-112">이 cmdlet이 runbook을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="5c79b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c79b-113">-DefaultProfile</span></span>
<span data-ttu-id="5c79b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c79b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c79b-115">-설명</span><span class="sxs-lookup"><span data-stu-id="5c79b-115">-Description</span></span>
<span data-ttu-id="5c79b-116">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="5c79b-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="5c79b-117">-LogProgress</span></span>
<span data-ttu-id="5c79b-118">Runbook이 진행률을 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="5c79b-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="5c79b-119">-LogVerbose</span></span>
<span data-ttu-id="5c79b-120">로깅에 자세한 정보가 포함 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="5c79b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="5c79b-121">-Name</span></span>
<span data-ttu-id="5c79b-122">이 cmdlet이 수정 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c79b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c79b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c79b-124">이 cmdlet이 runbook을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="5c79b-125">태그</span><span class="sxs-lookup"><span data-stu-id="5c79b-125">-Tag</span></span>
<span data-ttu-id="5c79b-126">Runbook 태그</span><span class="sxs-lookup"><span data-stu-id="5c79b-126">The runbook tags.</span></span>

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

### <span data-ttu-id="5c79b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c79b-127">CommonParameters</span></span>
<span data-ttu-id="5c79b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c79b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c79b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c79b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c79b-130">입력</span><span class="sxs-lookup"><span data-stu-id="5c79b-130">INPUTS</span></span>

### <span data-ttu-id="5c79b-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5c79b-131">System.String</span></span>

### <span data-ttu-id="5c79b-132">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="5c79b-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="5c79b-133">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5c79b-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5c79b-134">출력</span><span class="sxs-lookup"><span data-stu-id="5c79b-134">OUTPUTS</span></span>

### <span data-ttu-id="5c79b-135">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="5c79b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="5c79b-136">NOTES</span></span>

## <span data-ttu-id="5c79b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c79b-137">RELATED LINKS</span></span>

[<span data-ttu-id="5c79b-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-140">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-141">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-142">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-143">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-144">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="5c79b-145">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5c79b-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


