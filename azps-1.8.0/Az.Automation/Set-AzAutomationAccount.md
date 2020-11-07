---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: b0bebe0f831cc4041ecdeeeaa3ec8066faeacc8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701512"
---
# <span data-ttu-id="e9a6b-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e9a6b-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="e9a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a6b-103">Automation 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="e9a6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9a6b-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9a6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e9a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a6b-106">**Set-AzAutomationAccount** Cmdlet은 Azure Automation 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="e9a6b-107">자동화 계정에 대 한 자세한 내용은 New-AzAutomationAccount cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e9a6b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e9a6b-108">EXAMPLES</span></span>

### <span data-ttu-id="e9a6b-109">예제 1: Automation 계정의 태그 설정</span><span class="sxs-lookup"><span data-stu-id="e9a6b-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="e9a6b-110">첫 번째 명령은 두 개의 키/값 쌍을 $Tags 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="e9a6b-111">두 번째 명령은 AutomationAccount01 이라는 자동화 계정에 대 한 $Tags의 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="e9a6b-112">예제 2: Automation 계정에 대 한 계획 변경</span><span class="sxs-lookup"><span data-stu-id="e9a6b-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="e9a6b-113">이 명령은 AutomationAccount01 이라는 Automation 계정에 대 한 계획을 기본으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="e9a6b-114">변수</span><span class="sxs-lookup"><span data-stu-id="e9a6b-114">PARAMETERS</span></span>

### <span data-ttu-id="e9a6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a6b-115">-DefaultProfile</span></span>
<span data-ttu-id="e9a6b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e9a6b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a6b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e9a6b-117">-Name</span></span>
<span data-ttu-id="e9a6b-118">이 cmdlet이 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e9a6b-119">-계획</span><span class="sxs-lookup"><span data-stu-id="e9a6b-119">-Plan</span></span>
<span data-ttu-id="e9a6b-120">Automation 계정에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="e9a6b-121">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-121">Valid values are:</span></span>
- <span data-ttu-id="e9a6b-122">기본적</span><span class="sxs-lookup"><span data-stu-id="e9a6b-122">Basic</span></span>
- <span data-ttu-id="e9a6b-123">비우거나</span><span class="sxs-lookup"><span data-stu-id="e9a6b-123">Free</span></span>

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

### <span data-ttu-id="e9a6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9a6b-125">이 cmdlet이 수정 하는 자동화 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e9a6b-126">태그</span><span class="sxs-lookup"><span data-stu-id="e9a6b-126">-Tags</span></span>
<span data-ttu-id="e9a6b-127">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9a6b-128">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e9a6b-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e9a6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a6b-129">CommonParameters</span></span>
<span data-ttu-id="e9a6b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a6b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a6b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a6b-132">입력</span><span class="sxs-lookup"><span data-stu-id="e9a6b-132">INPUTS</span></span>

### <span data-ttu-id="e9a6b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e9a6b-133">System.String</span></span>

### <span data-ttu-id="e9a6b-134">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="e9a6b-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="e9a6b-135">출력</span><span class="sxs-lookup"><span data-stu-id="e9a6b-135">OUTPUTS</span></span>

### <span data-ttu-id="e9a6b-136">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="e9a6b-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e9a6b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e9a6b-137">NOTES</span></span>

## <span data-ttu-id="e9a6b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9a6b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9a6b-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e9a6b-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="e9a6b-140">새로운 AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e9a6b-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="e9a6b-141">제거-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e9a6b-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)