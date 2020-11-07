---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701519"
---
# <span data-ttu-id="5521a-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="5521a-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="5521a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5521a-102">SYNOPSIS</span></span>
<span data-ttu-id="5521a-103">Azure Automation 원본 컨트롤을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="5521a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5521a-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5521a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5521a-105">DESCRIPTION</span></span>
<span data-ttu-id="5521a-106">Remove-AzAutomationSourceControl cmdlet은 Azure Automation에서 소스 제어를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="5521a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5521a-107">EXAMPLES</span></span>

### <span data-ttu-id="5521a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5521a-108">Example 1</span></span>
<span data-ttu-id="5521a-109">이 명령은 devAccount 라는 계정에서 VSTSNative 이라는 자동화 원본 컨트롤을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="5521a-110">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="5521a-111">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="5521a-112">변수</span><span class="sxs-lookup"><span data-stu-id="5521a-112">PARAMETERS</span></span>

### <span data-ttu-id="5521a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5521a-113">-AutomationAccountName</span></span>
<span data-ttu-id="5521a-114">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-114">The automation account name.</span></span>

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

### <span data-ttu-id="5521a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5521a-115">-DefaultProfile</span></span>
<span data-ttu-id="5521a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5521a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5521a-117">-Name</span></span>
<span data-ttu-id="5521a-118">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-118">The source control name.</span></span>

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

### <span data-ttu-id="5521a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5521a-119">-PassThru</span></span>
<span data-ttu-id="5521a-120">PassThru 작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5521a-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5521a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5521a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5521a-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-123">The resource group name.</span></span>

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

### <span data-ttu-id="5521a-124">-확인</span><span class="sxs-lookup"><span data-stu-id="5521a-124">-Confirm</span></span>
<span data-ttu-id="5521a-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5521a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5521a-126">-WhatIf</span></span>
<span data-ttu-id="5521a-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5521a-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5521a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5521a-129">CommonParameters</span></span>
<span data-ttu-id="5521a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5521a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5521a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5521a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5521a-132">입력</span><span class="sxs-lookup"><span data-stu-id="5521a-132">INPUTS</span></span>

### <span data-ttu-id="5521a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5521a-133">System.String</span></span>

## <span data-ttu-id="5521a-134">출력</span><span class="sxs-lookup"><span data-stu-id="5521a-134">OUTPUTS</span></span>

### <span data-ttu-id="5521a-135">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="5521a-135">System.Void</span></span>

### <span data-ttu-id="5521a-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5521a-136">System.Boolean</span></span>

## <span data-ttu-id="5521a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="5521a-137">NOTES</span></span>

## <span data-ttu-id="5521a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5521a-138">RELATED LINKS</span></span>
