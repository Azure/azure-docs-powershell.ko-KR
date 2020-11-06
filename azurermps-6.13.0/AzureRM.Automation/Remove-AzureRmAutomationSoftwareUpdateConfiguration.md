---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528655"
---
# <span data-ttu-id="6576f-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6576f-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6576f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6576f-102">SYNOPSIS</span></span>
<span data-ttu-id="6576f-103">Azure automation 소프트웨어 업데이트 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6576f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6576f-104">SYNTAX</span></span>

### <span data-ttu-id="6576f-105">BySucName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6576f-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6576f-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="6576f-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6576f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6576f-107">DESCRIPTION</span></span>
<span data-ttu-id="6576f-108">이 cmdlet은 azure automation 소프트웨어 업데이트 구성을 제거 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="6576f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6576f-109">EXAMPLES</span></span>

### <span data-ttu-id="6576f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6576f-110">Example 1</span></span>
<span data-ttu-id="6576f-111">이 예제에서는 automation 계정에서 ' MyUpdateConfiguration '을 제거 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="6576f-112">변수</span><span class="sxs-lookup"><span data-stu-id="6576f-112">PARAMETERS</span></span>

### <span data-ttu-id="6576f-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6576f-113">-AutomationAccountName</span></span>
<span data-ttu-id="6576f-114">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-114">The automation account name.</span></span>

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

### <span data-ttu-id="6576f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6576f-115">-DefaultProfile</span></span>
<span data-ttu-id="6576f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6576f-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6576f-117">-Name</span></span>
<span data-ttu-id="6576f-118">제거할 소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6576f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6576f-119">-PassThru</span></span>
<span data-ttu-id="6576f-120">PassThru 작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6576f-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6576f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6576f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6576f-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-123">The resource group name.</span></span>

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

### <span data-ttu-id="6576f-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6576f-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="6576f-125">제거할 소프트웨어 업데이트 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6576f-126">-확인</span><span class="sxs-lookup"><span data-stu-id="6576f-126">-Confirm</span></span>
<span data-ttu-id="6576f-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6576f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6576f-128">-WhatIf</span></span>
<span data-ttu-id="6576f-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6576f-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6576f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6576f-131">CommonParameters</span></span>
<span data-ttu-id="6576f-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6576f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6576f-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6576f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6576f-134">입력</span><span class="sxs-lookup"><span data-stu-id="6576f-134">INPUTS</span></span>

### <span data-ttu-id="6576f-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6576f-135">System.String</span></span>

### <span data-ttu-id="6576f-136">UpdateManagement. SoftwareUpdateConfiguration에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="6576f-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6576f-137">출력</span><span class="sxs-lookup"><span data-stu-id="6576f-137">OUTPUTS</span></span>

### <span data-ttu-id="6576f-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="6576f-138">System.Object</span></span>
## <span data-ttu-id="6576f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6576f-139">NOTES</span></span>

## <span data-ttu-id="6576f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6576f-140">RELATED LINKS</span></span>
