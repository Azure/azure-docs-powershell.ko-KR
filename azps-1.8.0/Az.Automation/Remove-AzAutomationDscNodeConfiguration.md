---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 938fde14fb62ea7f7fd4e04baf5e309615957799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701531"
---
# <span data-ttu-id="ed5da-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed5da-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="ed5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed5da-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5da-103">자동화의 DSC 노드 구성에서 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="ed5da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed5da-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5da-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed5da-105">DESCRIPTION</span></span>
<span data-ttu-id="ed5da-106">**AzAutomationDscNodeConfiguration** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 노드 구성에서 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="ed5da-107">자동화는 DSC 노드 구성을 MOF (관리 개체 형식) 구성 문서로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="ed5da-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ed5da-108">EXAMPLES</span></span>

## <span data-ttu-id="ed5da-109">변수</span><span class="sxs-lookup"><span data-stu-id="ed5da-109">PARAMETERS</span></span>

### <span data-ttu-id="ed5da-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed5da-110">-AutomationAccountName</span></span>
<span data-ttu-id="ed5da-111">이 cmdlet이 메타 데이터를 제거 하는 DSC 노드 구성을 포함 하는 자동화 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="ed5da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5da-112">-DefaultProfile</span></span>
<span data-ttu-id="ed5da-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ed5da-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed5da-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5da-114">-Force</span></span>
<span data-ttu-id="ed5da-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="ed5da-115">ps_force</span></span>

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

### <span data-ttu-id="ed5da-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="ed5da-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="ed5da-117">이 cmdlet이 노드 매핑을 무시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5da-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ed5da-118">-Name</span></span>
<span data-ttu-id="ed5da-119">이 cmdlet이 메타 데이터를 제거 하는 DSC 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5da-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5da-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed5da-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ed5da-122">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 DSC 노드 구성에 대 한 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed5da-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ed5da-123">-Confirm</span></span>
<span data-ttu-id="ed5da-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5da-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5da-125">-WhatIf</span></span>
<span data-ttu-id="ed5da-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5da-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5da-128">CommonParameters</span></span>
<span data-ttu-id="ed5da-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed5da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5da-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5da-131">입력</span><span class="sxs-lookup"><span data-stu-id="ed5da-131">INPUTS</span></span>

### <span data-ttu-id="ed5da-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed5da-132">System.String</span></span>

## <span data-ttu-id="ed5da-133">출력</span><span class="sxs-lookup"><span data-stu-id="ed5da-133">OUTPUTS</span></span>

### <span data-ttu-id="ed5da-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ed5da-134">System.Void</span></span>

## <span data-ttu-id="ed5da-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ed5da-135">NOTES</span></span>

## <span data-ttu-id="ed5da-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed5da-136">RELATED LINKS</span></span>

[<span data-ttu-id="ed5da-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed5da-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ed5da-138">가져오기-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed5da-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ed5da-139">Azure 자동화 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ed5da-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)

