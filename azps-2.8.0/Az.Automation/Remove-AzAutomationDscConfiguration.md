---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: 1a556a92d59830a4be331c8415fde0c85ddba539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697763"
---
# <span data-ttu-id="63485-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63485-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="63485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63485-102">SYNOPSIS</span></span>
<span data-ttu-id="63485-103">자동화에서 DSC 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="63485-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63485-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63485-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63485-105">DESCRIPTION</span></span>
<span data-ttu-id="63485-106">**AzAutomationDscConfiguration** Cmdlet은 Azure 자동화에서 APS (원하는 상태 구성) 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="63485-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63485-107">EXAMPLES</span></span>

## <span data-ttu-id="63485-108">변수</span><span class="sxs-lookup"><span data-stu-id="63485-108">PARAMETERS</span></span>

### <span data-ttu-id="63485-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63485-109">-AutomationAccountName</span></span>
<span data-ttu-id="63485-110">이 cmdlet이 제거 하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63485-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63485-111">-DefaultProfile</span></span>
<span data-ttu-id="63485-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="63485-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63485-113">-Force</span><span class="sxs-lookup"><span data-stu-id="63485-113">-Force</span></span>
<span data-ttu-id="63485-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="63485-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63485-115">-이름</span><span class="sxs-lookup"><span data-stu-id="63485-115">-Name</span></span>
<span data-ttu-id="63485-116">이 cmdlet이 제거 하는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63485-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63485-117">-ResourceGroupName</span></span>
<span data-ttu-id="63485-118">이 cmdlet에서 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="63485-119">-확인</span><span class="sxs-lookup"><span data-stu-id="63485-119">-Confirm</span></span>
<span data-ttu-id="63485-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63485-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63485-121">-WhatIf</span></span>
<span data-ttu-id="63485-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63485-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63485-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63485-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63485-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63485-124">CommonParameters</span></span>
<span data-ttu-id="63485-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63485-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63485-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63485-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63485-127">입력</span><span class="sxs-lookup"><span data-stu-id="63485-127">INPUTS</span></span>

### <span data-ttu-id="63485-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63485-128">System.String</span></span>

## <span data-ttu-id="63485-129">출력</span><span class="sxs-lookup"><span data-stu-id="63485-129">OUTPUTS</span></span>

### <span data-ttu-id="63485-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="63485-130">System.Void</span></span>

## <span data-ttu-id="63485-131">상속자</span><span class="sxs-lookup"><span data-stu-id="63485-131">NOTES</span></span>

## <span data-ttu-id="63485-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63485-132">RELATED LINKS</span></span>

[<span data-ttu-id="63485-133">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63485-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="63485-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63485-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="63485-135">가져오기-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63485-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


