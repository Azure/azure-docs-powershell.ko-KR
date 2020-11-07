---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711443"
---
# <span data-ttu-id="22306-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22306-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="22306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22306-102">SYNOPSIS</span></span>
<span data-ttu-id="22306-103">자동화 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22306-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22306-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22306-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22306-105">DESCRIPTION</span></span>
<span data-ttu-id="22306-106">**AzureRmAutomationCredential** Cmdlet은 Azure Automation에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="22306-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22306-107">EXAMPLES</span></span>

### <span data-ttu-id="22306-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="22306-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="22306-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 ContosoCredential 이라는 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="22306-110">변수</span><span class="sxs-lookup"><span data-stu-id="22306-110">PARAMETERS</span></span>

### <span data-ttu-id="22306-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22306-111">-AutomationAccountName</span></span>
<span data-ttu-id="22306-112">이 cmdlet에서 자격 증명을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="22306-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22306-113">-DefaultProfile</span></span>
<span data-ttu-id="22306-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22306-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22306-115">-이름</span><span class="sxs-lookup"><span data-stu-id="22306-115">-Name</span></span>
<span data-ttu-id="22306-116">이 cmdlet이 제거 하는 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22306-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22306-117">-ResourceGroupName</span></span>
<span data-ttu-id="22306-118">이 cmdlet에서 자격 증명을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="22306-119">-확인</span><span class="sxs-lookup"><span data-stu-id="22306-119">-Confirm</span></span>
<span data-ttu-id="22306-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22306-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22306-121">-WhatIf</span></span>
<span data-ttu-id="22306-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22306-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22306-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22306-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22306-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22306-124">CommonParameters</span></span>
<span data-ttu-id="22306-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22306-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22306-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22306-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22306-127">입력</span><span class="sxs-lookup"><span data-stu-id="22306-127">INPUTS</span></span>

### <span data-ttu-id="22306-128">않아야</span><span class="sxs-lookup"><span data-stu-id="22306-128">None</span></span>
<span data-ttu-id="22306-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22306-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22306-130">출력</span><span class="sxs-lookup"><span data-stu-id="22306-130">OUTPUTS</span></span>

## <span data-ttu-id="22306-131">상속자</span><span class="sxs-lookup"><span data-stu-id="22306-131">NOTES</span></span>

## <span data-ttu-id="22306-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22306-132">RELATED LINKS</span></span>

[<span data-ttu-id="22306-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22306-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="22306-134">새로운 AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22306-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="22306-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22306-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


