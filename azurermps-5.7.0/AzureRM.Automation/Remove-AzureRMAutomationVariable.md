---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530566"
---
# <span data-ttu-id="50053-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="50053-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="50053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50053-102">SYNOPSIS</span></span>
<span data-ttu-id="50053-103">자동화 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50053-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50053-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50053-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50053-105">DESCRIPTION</span></span>
<span data-ttu-id="50053-106">**AzureRmAutomationVariable** Cmdlet은 Azure 자동화에서 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="50053-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50053-107">EXAMPLES</span></span>

### <span data-ttu-id="50053-108">예제 1: 변수 제거</span><span class="sxs-lookup"><span data-stu-id="50053-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="50053-109">이 명령은 Contoso17 이라는 Automation 계정에서 StringVariable22 이라는 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="50053-110">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="50053-111">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50053-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="50053-112">변수</span><span class="sxs-lookup"><span data-stu-id="50053-112">PARAMETERS</span></span>

### <span data-ttu-id="50053-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="50053-113">-AutomationAccountName</span></span>
<span data-ttu-id="50053-114">이 cmdlet이 삭제 하는 변수를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="50053-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50053-115">-DefaultProfile</span></span>
<span data-ttu-id="50053-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="50053-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50053-117">-이름</span><span class="sxs-lookup"><span data-stu-id="50053-117">-Name</span></span>
<span data-ttu-id="50053-118">이 cmdlet이 삭제 하는 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50053-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50053-119">-ResourceGroupName</span></span>
<span data-ttu-id="50053-120">이 cmdlet이 변수를 삭제할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="50053-121">-확인</span><span class="sxs-lookup"><span data-stu-id="50053-121">-Confirm</span></span>
<span data-ttu-id="50053-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50053-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50053-123">-WhatIf</span></span>
<span data-ttu-id="50053-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50053-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50053-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50053-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50053-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50053-126">CommonParameters</span></span>
<span data-ttu-id="50053-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50053-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50053-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50053-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50053-129">입력</span><span class="sxs-lookup"><span data-stu-id="50053-129">INPUTS</span></span>

### <span data-ttu-id="50053-130">않아야</span><span class="sxs-lookup"><span data-stu-id="50053-130">None</span></span>
<span data-ttu-id="50053-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50053-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50053-132">출력</span><span class="sxs-lookup"><span data-stu-id="50053-132">OUTPUTS</span></span>

### <span data-ttu-id="50053-133">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="50053-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="50053-134">상속자</span><span class="sxs-lookup"><span data-stu-id="50053-134">NOTES</span></span>

## <span data-ttu-id="50053-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50053-135">RELATED LINKS</span></span>

[<span data-ttu-id="50053-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="50053-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="50053-137">새로운 AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="50053-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="50053-138">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="50053-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


