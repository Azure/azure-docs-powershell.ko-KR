---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494232"
---
# <span data-ttu-id="607c4-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="607c4-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="607c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607c4-102">SYNOPSIS</span></span>
<span data-ttu-id="607c4-103">Azure Automation 원본 제어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="607c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="607c4-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="607c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="607c4-105">DESCRIPTION</span></span>
<span data-ttu-id="607c4-106">이 Remove-AzAutomationSourceControl cmdlet은 Azure Automation에서 원본 제어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="607c4-107">예제</span><span class="sxs-lookup"><span data-stu-id="607c4-107">EXAMPLES</span></span>

### <span data-ttu-id="607c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="607c4-108">Example 1</span></span>
<span data-ttu-id="607c4-109">이 명령은 devAccount라는 계정에서 VSTSNative라는 Automation 소스 제어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="607c4-110">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="607c4-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="607c4-111">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="607c4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607c4-112">PARAMETERS</span></span>

### <span data-ttu-id="607c4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="607c4-113">-AutomationAccountName</span></span>
<span data-ttu-id="607c4-114">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-114">The automation account name.</span></span>

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

### <span data-ttu-id="607c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607c4-115">-DefaultProfile</span></span>
<span data-ttu-id="607c4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="607c4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="607c4-117">-Name</span></span>
<span data-ttu-id="607c4-118">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-118">The source control name.</span></span>

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

### <span data-ttu-id="607c4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="607c4-119">-PassThru</span></span>
<span data-ttu-id="607c4-120">PassThru는 작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="607c4-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="607c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="607c4-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-123">The resource group name.</span></span>

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

### <span data-ttu-id="607c4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="607c4-124">-Confirm</span></span>
<span data-ttu-id="607c4-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="607c4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607c4-126">-WhatIf</span></span>
<span data-ttu-id="607c4-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="607c4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607c4-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="607c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607c4-129">CommonParameters</span></span>
<span data-ttu-id="607c4-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="607c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607c4-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="607c4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607c4-132">입력</span><span class="sxs-lookup"><span data-stu-id="607c4-132">INPUTS</span></span>

### <span data-ttu-id="607c4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="607c4-133">System.String</span></span>

## <span data-ttu-id="607c4-134">출력</span><span class="sxs-lookup"><span data-stu-id="607c4-134">OUTPUTS</span></span>

### <span data-ttu-id="607c4-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="607c4-135">System.Void</span></span>

### <span data-ttu-id="607c4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="607c4-136">System.Boolean</span></span>

## <span data-ttu-id="607c4-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="607c4-137">NOTES</span></span>

## <span data-ttu-id="607c4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="607c4-138">RELATED LINKS</span></span>
