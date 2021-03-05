---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009856"
---
# <span data-ttu-id="5bdd1-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="5bdd1-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="5bdd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bdd1-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdd1-103">Azure Automation 원본 컨트롤을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="5bdd1-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bdd1-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bdd1-105">설명</span><span class="sxs-lookup"><span data-stu-id="5bdd1-105">DESCRIPTION</span></span>
<span data-ttu-id="5bdd1-106">Remove-AzAutomationSourceControl cmdlet은 Azure Automation에서 원본 컨트롤을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="5bdd1-107">예제</span><span class="sxs-lookup"><span data-stu-id="5bdd1-107">EXAMPLES</span></span>

### <span data-ttu-id="5bdd1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bdd1-108">Example 1</span></span>
<span data-ttu-id="5bdd1-109">이 명령은 devAccount라는 계정에서 VSTSNative라는 Automation 원본 컨트롤을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="5bdd1-110">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="5bdd1-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="5bdd1-111">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="5bdd1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5bdd1-112">PARAMETERS</span></span>

### <span data-ttu-id="5bdd1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5bdd1-113">-AutomationAccountName</span></span>
<span data-ttu-id="5bdd1-114">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-114">The automation account name.</span></span>

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

### <span data-ttu-id="5bdd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdd1-115">-DefaultProfile</span></span>
<span data-ttu-id="5bdd1-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bdd1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5bdd1-117">-Name</span></span>
<span data-ttu-id="5bdd1-118">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-118">The source control name.</span></span>

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

### <span data-ttu-id="5bdd1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bdd1-119">-PassThru</span></span>
<span data-ttu-id="5bdd1-120">PassThru는 작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5bdd1-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5bdd1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bdd1-122">-ResourceGroupName</span></span>
<span data-ttu-id="5bdd1-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-123">The resource group name.</span></span>

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

### <span data-ttu-id="5bdd1-124">-확인</span><span class="sxs-lookup"><span data-stu-id="5bdd1-124">-Confirm</span></span>
<span data-ttu-id="5bdd1-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdd1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdd1-126">-WhatIf</span></span>
<span data-ttu-id="5bdd1-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bdd1-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdd1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdd1-129">CommonParameters</span></span>
<span data-ttu-id="5bdd1-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdd1-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5bdd1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdd1-132">입력</span><span class="sxs-lookup"><span data-stu-id="5bdd1-132">INPUTS</span></span>

### <span data-ttu-id="5bdd1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5bdd1-133">System.String</span></span>

## <span data-ttu-id="5bdd1-134">출력</span><span class="sxs-lookup"><span data-stu-id="5bdd1-134">OUTPUTS</span></span>

### <span data-ttu-id="5bdd1-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="5bdd1-135">System.Void</span></span>

### <span data-ttu-id="5bdd1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bdd1-136">System.Boolean</span></span>

## <span data-ttu-id="5bdd1-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bdd1-137">NOTES</span></span>

## <span data-ttu-id="5bdd1-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bdd1-138">RELATED LINKS</span></span>
