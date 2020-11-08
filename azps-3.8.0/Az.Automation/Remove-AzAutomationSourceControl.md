---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044921"
---
# <span data-ttu-id="4f16d-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="4f16d-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="4f16d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f16d-102">SYNOPSIS</span></span>
<span data-ttu-id="4f16d-103">Azure Automation 원본 컨트롤을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="4f16d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f16d-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f16d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f16d-105">DESCRIPTION</span></span>
<span data-ttu-id="4f16d-106">Remove-AzAutomationSourceControl cmdlet은 Azure Automation에서 소스 제어를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="4f16d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4f16d-107">EXAMPLES</span></span>

### <span data-ttu-id="4f16d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f16d-108">Example 1</span></span>
<span data-ttu-id="4f16d-109">이 명령은 devAccount 라는 계정에서 VSTSNative 이라는 자동화 원본 컨트롤을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="4f16d-110">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="4f16d-111">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="4f16d-112">변수</span><span class="sxs-lookup"><span data-stu-id="4f16d-112">PARAMETERS</span></span>

### <span data-ttu-id="4f16d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4f16d-113">-AutomationAccountName</span></span>
<span data-ttu-id="4f16d-114">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-114">The automation account name.</span></span>

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

### <span data-ttu-id="4f16d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f16d-115">-DefaultProfile</span></span>
<span data-ttu-id="4f16d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f16d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4f16d-117">-Name</span></span>
<span data-ttu-id="4f16d-118">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-118">The source control name.</span></span>

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

### <span data-ttu-id="4f16d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f16d-119">-PassThru</span></span>
<span data-ttu-id="4f16d-120">PassThru 작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f16d-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f16d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f16d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f16d-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-123">The resource group name.</span></span>

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

### <span data-ttu-id="4f16d-124">-확인</span><span class="sxs-lookup"><span data-stu-id="4f16d-124">-Confirm</span></span>
<span data-ttu-id="4f16d-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f16d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f16d-126">-WhatIf</span></span>
<span data-ttu-id="4f16d-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f16d-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f16d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f16d-129">CommonParameters</span></span>
<span data-ttu-id="4f16d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f16d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f16d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f16d-132">입력</span><span class="sxs-lookup"><span data-stu-id="4f16d-132">INPUTS</span></span>

### <span data-ttu-id="4f16d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f16d-133">System.String</span></span>

## <span data-ttu-id="4f16d-134">출력</span><span class="sxs-lookup"><span data-stu-id="4f16d-134">OUTPUTS</span></span>

### <span data-ttu-id="4f16d-135">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4f16d-135">System.Void</span></span>

### <span data-ttu-id="4f16d-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4f16d-136">System.Boolean</span></span>

## <span data-ttu-id="4f16d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4f16d-137">NOTES</span></span>

## <span data-ttu-id="4f16d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f16d-138">RELATED LINKS</span></span>
