---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531856"
---
# <span data-ttu-id="33e89-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="33e89-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="33e89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e89-102">SYNOPSIS</span></span>
<span data-ttu-id="33e89-103">Automation 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33e89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33e89-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33e89-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33e89-105">DESCRIPTION</span></span>
<span data-ttu-id="33e89-106">**AzureRmAutomationSchedule** Cmdlet은 Azure 자동화에서 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="33e89-107">예제의</span><span class="sxs-lookup"><span data-stu-id="33e89-107">EXAMPLES</span></span>

### <span data-ttu-id="33e89-108">예제 1: 일정 제거</span><span class="sxs-lookup"><span data-stu-id="33e89-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="33e89-109">이 명령은 Schedule01 이라는 일정에 대 한 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="33e89-110">변수</span><span class="sxs-lookup"><span data-stu-id="33e89-110">PARAMETERS</span></span>

### <span data-ttu-id="33e89-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33e89-111">-AutomationAccountName</span></span>
<span data-ttu-id="33e89-112">이 cmdlet이 일정을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="33e89-113">-Force</span><span class="sxs-lookup"><span data-stu-id="33e89-113">-Force</span></span>
<span data-ttu-id="33e89-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="33e89-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e89-115">-이름</span><span class="sxs-lookup"><span data-stu-id="33e89-115">-Name</span></span>
<span data-ttu-id="33e89-116">이 cmdlet이 제거 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e89-117">-ResourceGroupName</span></span>
<span data-ttu-id="33e89-118">이 cmdlet이 일정을 제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="33e89-119">-확인</span><span class="sxs-lookup"><span data-stu-id="33e89-119">-Confirm</span></span>
<span data-ttu-id="33e89-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e89-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33e89-121">-WhatIf</span></span>
<span data-ttu-id="33e89-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33e89-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e89-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e89-124">-DefaultProfile</span></span>
<span data-ttu-id="33e89-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e89-126">CommonParameters</span></span>
<span data-ttu-id="33e89-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e89-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e89-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e89-129">입력</span><span class="sxs-lookup"><span data-stu-id="33e89-129">INPUTS</span></span>

## <span data-ttu-id="33e89-130">출력</span><span class="sxs-lookup"><span data-stu-id="33e89-130">OUTPUTS</span></span>

## <span data-ttu-id="33e89-131">상속자</span><span class="sxs-lookup"><span data-stu-id="33e89-131">NOTES</span></span>

## <span data-ttu-id="33e89-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33e89-132">RELATED LINKS</span></span>

[<span data-ttu-id="33e89-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="33e89-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="33e89-134">새로운 AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="33e89-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="33e89-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="33e89-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


