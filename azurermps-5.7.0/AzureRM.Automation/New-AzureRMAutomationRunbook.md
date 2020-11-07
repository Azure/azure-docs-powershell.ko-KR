---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704190"
---
# <span data-ttu-id="cd988-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="cd988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd988-102">SYNOPSIS</span></span>
<span data-ttu-id="cd988-103">자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd988-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd988-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd988-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd988-105">DESCRIPTION</span></span>
<span data-ttu-id="cd988-106">**AzureRmAutomationRunbook** CMDLET은 ap를 사용 하 여 빈 Azure 자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="cd988-107">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="cd988-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cd988-108">EXAMPLES</span></span>

### <span data-ttu-id="cd988-109">예제 1: runbook 만들기</span><span class="sxs-lookup"><span data-stu-id="cd988-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cd988-110">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbook02 라는 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cd988-111">변수</span><span class="sxs-lookup"><span data-stu-id="cd988-111">PARAMETERS</span></span>

### <span data-ttu-id="cd988-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd988-112">-AutomationAccountName</span></span>
<span data-ttu-id="cd988-113">이 cmdlet이 runbook을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="cd988-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd988-114">-DefaultProfile</span></span>
<span data-ttu-id="cd988-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cd988-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd988-116">-설명</span><span class="sxs-lookup"><span data-stu-id="cd988-116">-Description</span></span>
<span data-ttu-id="cd988-117">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-117">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd988-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="cd988-118">-LogProgress</span></span>
<span data-ttu-id="cd988-119">Runbook이 진행률을 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd988-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="cd988-120">-LogVerbose</span></span>
<span data-ttu-id="cd988-121">로깅에 자세한 정보가 포함 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd988-122">-이름</span><span class="sxs-lookup"><span data-stu-id="cd988-122">-Name</span></span>
<span data-ttu-id="cd988-123">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-123">Specifies a name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd988-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd988-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd988-125">이 cmdlet이 runbook을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="cd988-126">태그</span><span class="sxs-lookup"><span data-stu-id="cd988-126">-Tags</span></span>
<span data-ttu-id="cd988-127">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd988-128">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="cd988-128">For example:</span></span>

<span data-ttu-id="cd988-129">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cd988-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd988-130">-Type</span><span class="sxs-lookup"><span data-stu-id="cd988-130">-Type</span></span>
<span data-ttu-id="cd988-131">이 cmdlet이 만드는 runbook의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="cd988-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-132">Valid values are:</span></span>

- <span data-ttu-id="cd988-133">슬래시</span><span class="sxs-lookup"><span data-stu-id="cd988-133">PowerShell</span></span>
- <span data-ttu-id="cd988-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="cd988-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="cd988-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="cd988-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="cd988-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="cd988-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="cd988-137">Graph</span><span class="sxs-lookup"><span data-stu-id="cd988-137">Graph</span></span>

<span data-ttu-id="cd988-138">값 그래프가 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="cd988-139">이는 GraphicalPowerShellWorkflow와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd988-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd988-140">CommonParameters</span></span>
<span data-ttu-id="cd988-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd988-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd988-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd988-143">입력</span><span class="sxs-lookup"><span data-stu-id="cd988-143">INPUTS</span></span>

### <span data-ttu-id="cd988-144">않아야</span><span class="sxs-lookup"><span data-stu-id="cd988-144">None</span></span>
<span data-ttu-id="cd988-145">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd988-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd988-146">출력</span><span class="sxs-lookup"><span data-stu-id="cd988-146">OUTPUTS</span></span>

### <span data-ttu-id="cd988-147">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="cd988-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="cd988-148">상속자</span><span class="sxs-lookup"><span data-stu-id="cd988-148">NOTES</span></span>

## <span data-ttu-id="cd988-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd988-149">RELATED LINKS</span></span>

[<span data-ttu-id="cd988-150">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd988-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd988-152">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd988-153">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd988-154">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd988-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cd988-156">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cd988-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
