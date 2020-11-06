---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531220"
---
# <span data-ttu-id="94c31-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="94c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c31-102">SYNOPSIS</span></span>
<span data-ttu-id="94c31-103">자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94c31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94c31-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94c31-105">설명은</span><span class="sxs-lookup"><span data-stu-id="94c31-105">DESCRIPTION</span></span>
<span data-ttu-id="94c31-106">**AzureRmAutomationRunbook** CMDLET은 ap를 사용 하 여 빈 Azure 자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="94c31-107">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="94c31-108">예제의</span><span class="sxs-lookup"><span data-stu-id="94c31-108">EXAMPLES</span></span>

### <span data-ttu-id="94c31-109">예제 1: runbook 만들기</span><span class="sxs-lookup"><span data-stu-id="94c31-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="94c31-110">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbook02 라는 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="94c31-111">변수</span><span class="sxs-lookup"><span data-stu-id="94c31-111">PARAMETERS</span></span>

### <span data-ttu-id="94c31-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94c31-112">-AutomationAccountName</span></span>
<span data-ttu-id="94c31-113">이 cmdlet이 runbook을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="94c31-114">-설명</span><span class="sxs-lookup"><span data-stu-id="94c31-114">-Description</span></span>
<span data-ttu-id="94c31-115">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="94c31-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="94c31-116">-LogProgress</span></span>
<span data-ttu-id="94c31-117">Runbook이 진행률을 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="94c31-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="94c31-118">-LogVerbose</span></span>
<span data-ttu-id="94c31-119">로깅에 자세한 정보가 포함 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="94c31-120">-이름</span><span class="sxs-lookup"><span data-stu-id="94c31-120">-Name</span></span>
<span data-ttu-id="94c31-121">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="94c31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c31-122">-ResourceGroupName</span></span>
<span data-ttu-id="94c31-123">이 cmdlet이 runbook을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="94c31-124">태그</span><span class="sxs-lookup"><span data-stu-id="94c31-124">-Tags</span></span>
<span data-ttu-id="94c31-125">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94c31-126">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="94c31-126">For example:</span></span>

<span data-ttu-id="94c31-127">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="94c31-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="94c31-128">-Type</span><span class="sxs-lookup"><span data-stu-id="94c31-128">-Type</span></span>
<span data-ttu-id="94c31-129">이 cmdlet이 만드는 runbook의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="94c31-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-130">Valid values are:</span></span>

- <span data-ttu-id="94c31-131">슬래시</span><span class="sxs-lookup"><span data-stu-id="94c31-131">PowerShell</span></span>
- <span data-ttu-id="94c31-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="94c31-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="94c31-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="94c31-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="94c31-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="94c31-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="94c31-135">Graph</span><span class="sxs-lookup"><span data-stu-id="94c31-135">Graph</span></span>

<span data-ttu-id="94c31-136">값 그래프가 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="94c31-137">이는 GraphicalPowerShellWorkflow와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c31-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c31-138">-DefaultProfile</span></span>
<span data-ttu-id="94c31-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94c31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c31-140">CommonParameters</span></span>
<span data-ttu-id="94c31-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94c31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c31-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c31-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c31-143">입력</span><span class="sxs-lookup"><span data-stu-id="94c31-143">INPUTS</span></span>

## <span data-ttu-id="94c31-144">출력</span><span class="sxs-lookup"><span data-stu-id="94c31-144">OUTPUTS</span></span>

### <span data-ttu-id="94c31-145">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="94c31-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="94c31-146">상속자</span><span class="sxs-lookup"><span data-stu-id="94c31-146">NOTES</span></span>

## <span data-ttu-id="94c31-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94c31-147">RELATED LINKS</span></span>

[<span data-ttu-id="94c31-148">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94c31-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94c31-150">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94c31-151">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94c31-152">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94c31-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94c31-154">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94c31-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
