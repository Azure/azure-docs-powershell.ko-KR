---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: 8866c805f0cbb42d72c8940d31652bc8e5444cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531852"
---
# <span data-ttu-id="7ea93-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7ea93-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="7ea93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea93-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea93-103">자동화 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea93-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ea93-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ea93-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7ea93-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea93-106">**AzureRmAutomationVariable** Cmdlet은 Azure 자동화에서 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="7ea93-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7ea93-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea93-108">예제 1: 변수 제거</span><span class="sxs-lookup"><span data-stu-id="7ea93-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ea93-109">이 명령은 Contoso17 이라는 Automation 계정에서 StringVariable22 이라는 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7ea93-110">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7ea93-111">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7ea93-112">변수</span><span class="sxs-lookup"><span data-stu-id="7ea93-112">PARAMETERS</span></span>

### <span data-ttu-id="7ea93-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ea93-113">-AutomationAccountName</span></span>
<span data-ttu-id="7ea93-114">이 cmdlet이 삭제 하는 변수를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7ea93-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7ea93-115">-Name</span></span>
<span data-ttu-id="7ea93-116">이 cmdlet이 삭제 하는 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-116">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7ea93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea93-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ea93-118">이 cmdlet이 변수를 삭제할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-118">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="7ea93-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7ea93-119">-Confirm</span></span>
<span data-ttu-id="7ea93-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea93-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea93-121">-WhatIf</span></span>
<span data-ttu-id="7ea93-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea93-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea93-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea93-124">-DefaultProfile</span></span>
<span data-ttu-id="7ea93-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea93-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea93-126">CommonParameters</span></span>
<span data-ttu-id="7ea93-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea93-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea93-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea93-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea93-129">입력</span><span class="sxs-lookup"><span data-stu-id="7ea93-129">INPUTS</span></span>

## <span data-ttu-id="7ea93-130">출력</span><span class="sxs-lookup"><span data-stu-id="7ea93-130">OUTPUTS</span></span>

### <span data-ttu-id="7ea93-131">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="7ea93-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="7ea93-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7ea93-132">NOTES</span></span>

## <span data-ttu-id="7ea93-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ea93-133">RELATED LINKS</span></span>

[<span data-ttu-id="7ea93-134">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7ea93-134">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="7ea93-135">새로운 AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7ea93-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="7ea93-136">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7ea93-136">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


