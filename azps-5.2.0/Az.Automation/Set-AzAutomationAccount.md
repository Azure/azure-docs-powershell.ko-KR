---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373143"
---
# <span data-ttu-id="36e75-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36e75-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="36e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e75-102">SYNOPSIS</span></span>
<span data-ttu-id="36e75-103">Automation 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="36e75-104">구문</span><span class="sxs-lookup"><span data-stu-id="36e75-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e75-105">설명</span><span class="sxs-lookup"><span data-stu-id="36e75-105">DESCRIPTION</span></span>
<span data-ttu-id="36e75-106">**Set-AzAutomationAccount** cmdlet은 Azure Automation 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="36e75-107">Automation 계정에 대한 자세한 내용은 다음 cmdlet을 New-AzAutomationAccount 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36e75-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="36e75-108">예제</span><span class="sxs-lookup"><span data-stu-id="36e75-108">EXAMPLES</span></span>

### <span data-ttu-id="36e75-109">예제 1: Automation 계정에 대한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="36e75-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="36e75-110">첫 번째 명령은 두 개의 키/값 쌍을 $Tags 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="36e75-111">두 번째 명령은 AutomationAccount01이라는 automation 계정에 $Tags 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="36e75-112">예제 2: Automation 계정에 대한 계획 변경</span><span class="sxs-lookup"><span data-stu-id="36e75-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="36e75-113">이 명령은 AutomationAccount01이라는 Automation 계정에 대한 계획을 Basic으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="36e75-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36e75-114">PARAMETERS</span></span>

### <span data-ttu-id="36e75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e75-115">-DefaultProfile</span></span>
<span data-ttu-id="36e75-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="36e75-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36e75-117">-Name</span><span class="sxs-lookup"><span data-stu-id="36e75-117">-Name</span></span>
<span data-ttu-id="36e75-118">이 cmdlet이 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e75-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="36e75-119">-Plan</span></span>
<span data-ttu-id="36e75-120">Automation 계정에 대한 계획을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="36e75-121">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="36e75-121">Valid values are:</span></span>
- <span data-ttu-id="36e75-122">기본</span><span class="sxs-lookup"><span data-stu-id="36e75-122">Basic</span></span>
- <span data-ttu-id="36e75-123">무료</span><span class="sxs-lookup"><span data-stu-id="36e75-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e75-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e75-124">-ResourceGroupName</span></span>
<span data-ttu-id="36e75-125">이 cmdlet이 수정하는 Automation 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="36e75-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="36e75-126">-Tags</span></span>
<span data-ttu-id="36e75-127">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36e75-128">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="36e75-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36e75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e75-129">CommonParameters</span></span>
<span data-ttu-id="36e75-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36e75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e75-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36e75-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e75-132">입력</span><span class="sxs-lookup"><span data-stu-id="36e75-132">INPUTS</span></span>

### <span data-ttu-id="36e75-133">System.String</span><span class="sxs-lookup"><span data-stu-id="36e75-133">System.String</span></span>

### <span data-ttu-id="36e75-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="36e75-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="36e75-135">출력</span><span class="sxs-lookup"><span data-stu-id="36e75-135">OUTPUTS</span></span>

### <span data-ttu-id="36e75-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36e75-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="36e75-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36e75-137">NOTES</span></span>

## <span data-ttu-id="36e75-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36e75-138">RELATED LINKS</span></span>

[<span data-ttu-id="36e75-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36e75-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="36e75-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36e75-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="36e75-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36e75-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
