---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697797"
---
# <span data-ttu-id="2139a-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="2139a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2139a-102">SYNOPSIS</span></span>
<span data-ttu-id="2139a-103">자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="2139a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2139a-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2139a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2139a-105">DESCRIPTION</span></span>
<span data-ttu-id="2139a-106">**AzAutomationRunbook** CMDLET은 ap를 사용 하 여 빈 Azure 자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="2139a-107">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="2139a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2139a-108">EXAMPLES</span></span>

### <span data-ttu-id="2139a-109">예제 1: runbook 만들기</span><span class="sxs-lookup"><span data-stu-id="2139a-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2139a-110">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbook02 라는 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2139a-111">변수</span><span class="sxs-lookup"><span data-stu-id="2139a-111">PARAMETERS</span></span>

### <span data-ttu-id="2139a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2139a-112">-AutomationAccountName</span></span>
<span data-ttu-id="2139a-113">이 cmdlet이 runbook을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="2139a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2139a-114">-DefaultProfile</span></span>
<span data-ttu-id="2139a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2139a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2139a-116">-설명</span><span class="sxs-lookup"><span data-stu-id="2139a-116">-Description</span></span>
<span data-ttu-id="2139a-117">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="2139a-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="2139a-118">-LogProgress</span></span>
<span data-ttu-id="2139a-119">Runbook이 진행률을 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="2139a-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="2139a-120">-LogVerbose</span></span>
<span data-ttu-id="2139a-121">로깅에 자세한 정보가 포함 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="2139a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2139a-122">-Name</span></span>
<span data-ttu-id="2139a-123">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="2139a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2139a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2139a-125">이 cmdlet이 runbook을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="2139a-126">태그</span><span class="sxs-lookup"><span data-stu-id="2139a-126">-Tags</span></span>
<span data-ttu-id="2139a-127">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2139a-128">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2139a-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-129">-Type</span><span class="sxs-lookup"><span data-stu-id="2139a-129">-Type</span></span>
<span data-ttu-id="2139a-130">이 cmdlet이 만드는 runbook의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="2139a-131">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-131">Valid values are:</span></span>
- <span data-ttu-id="2139a-132">슬래시</span><span class="sxs-lookup"><span data-stu-id="2139a-132">PowerShell</span></span>
- <span data-ttu-id="2139a-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="2139a-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="2139a-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="2139a-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="2139a-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="2139a-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="2139a-136">Graph</span><span class="sxs-lookup"><span data-stu-id="2139a-136">Graph</span></span>
- <span data-ttu-id="2139a-137">Python2 값 그래프는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="2139a-138">이는 GraphicalPowerShellWorkflow와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2139a-139">CommonParameters</span></span>
<span data-ttu-id="2139a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2139a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2139a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2139a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2139a-142">입력</span><span class="sxs-lookup"><span data-stu-id="2139a-142">INPUTS</span></span>

### <span data-ttu-id="2139a-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2139a-143">System.String</span></span>

### <span data-ttu-id="2139a-144">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="2139a-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="2139a-145">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2139a-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2139a-146">출력</span><span class="sxs-lookup"><span data-stu-id="2139a-146">OUTPUTS</span></span>

### <span data-ttu-id="2139a-147">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="2139a-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="2139a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="2139a-148">NOTES</span></span>

## <span data-ttu-id="2139a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2139a-149">RELATED LINKS</span></span>

[<span data-ttu-id="2139a-150">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="2139a-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2139a-152">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2139a-153">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2139a-154">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2139a-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="2139a-156">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2139a-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
