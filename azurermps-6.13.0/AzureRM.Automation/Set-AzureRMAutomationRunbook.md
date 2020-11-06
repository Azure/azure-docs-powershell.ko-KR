---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 26f3214cf98e43a805aab99eb3ad1b92f289b2bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529641"
---
# <span data-ttu-id="72a67-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="72a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72a67-102">SYNOPSIS</span></span>
<span data-ttu-id="72a67-103">Runbook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72a67-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72a67-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72a67-105">DESCRIPTION</span></span>
<span data-ttu-id="72a67-106">**AzureRmAutomationRunbook** CMDLET은 APS에서 Azure 자동화 runbook의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="72a67-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72a67-107">EXAMPLES</span></span>

### <span data-ttu-id="72a67-108">예제 1: runbook에 대 한 자세한 로깅 설정</span><span class="sxs-lookup"><span data-stu-id="72a67-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="72a67-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 지정 된 runbook의 작업에 대 한 자세한 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="72a67-110">변수</span><span class="sxs-lookup"><span data-stu-id="72a67-110">PARAMETERS</span></span>

### <span data-ttu-id="72a67-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72a67-111">-AutomationAccountName</span></span>
<span data-ttu-id="72a67-112">이 cmdlet이 runbook을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="72a67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a67-113">-DefaultProfile</span></span>
<span data-ttu-id="72a67-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="72a67-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72a67-115">-설명</span><span class="sxs-lookup"><span data-stu-id="72a67-115">-Description</span></span>
<span data-ttu-id="72a67-116">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="72a67-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="72a67-117">-LogProgress</span></span>
<span data-ttu-id="72a67-118">Runbook이 진행률을 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="72a67-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="72a67-119">-LogVerbose</span></span>
<span data-ttu-id="72a67-120">로깅에 자세한 정보가 포함 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="72a67-121">-이름</span><span class="sxs-lookup"><span data-stu-id="72a67-121">-Name</span></span>
<span data-ttu-id="72a67-122">이 cmdlet이 수정 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="72a67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a67-123">-ResourceGroupName</span></span>
<span data-ttu-id="72a67-124">이 cmdlet이 runbook을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="72a67-125">태그</span><span class="sxs-lookup"><span data-stu-id="72a67-125">-Tag</span></span>
<span data-ttu-id="72a67-126">Runbook 태그</span><span class="sxs-lookup"><span data-stu-id="72a67-126">The runbook tags.</span></span>

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

### <span data-ttu-id="72a67-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a67-127">CommonParameters</span></span>
<span data-ttu-id="72a67-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72a67-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a67-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a67-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a67-130">입력</span><span class="sxs-lookup"><span data-stu-id="72a67-130">INPUTS</span></span>

### <span data-ttu-id="72a67-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72a67-131">System.String</span></span>

### <span data-ttu-id="72a67-132">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="72a67-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="72a67-133">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="72a67-133">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="72a67-134">출력</span><span class="sxs-lookup"><span data-stu-id="72a67-134">OUTPUTS</span></span>

### <span data-ttu-id="72a67-135">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="72a67-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="72a67-136">상속자</span><span class="sxs-lookup"><span data-stu-id="72a67-136">NOTES</span></span>

## <span data-ttu-id="72a67-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72a67-137">RELATED LINKS</span></span>

[<span data-ttu-id="72a67-138">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-138">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-139">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-139">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-140">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-140">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-141">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-142">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-142">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-143">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-143">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-144">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-144">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="72a67-145">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72a67-145">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


