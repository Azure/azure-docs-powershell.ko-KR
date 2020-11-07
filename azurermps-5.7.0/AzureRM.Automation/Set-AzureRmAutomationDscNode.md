---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702390"
---
# <span data-ttu-id="76c88-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="76c88-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="76c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c88-102">SYNOPSIS</span></span>
<span data-ttu-id="76c88-103">DSC 노드가 매핑되는 노드 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76c88-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76c88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76c88-105">DESCRIPTION</span></span>
<span data-ttu-id="76c88-106">**AzureRmAutomationDscNode** CMDLET은 Ap (원하는 상태 구성) 노드 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="76c88-107">Azure 자동화는 DSC 노드 구성을 MOF (관리 개체 형식) 구성 문서로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="76c88-108">예제의</span><span class="sxs-lookup"><span data-stu-id="76c88-108">EXAMPLES</span></span>

### <span data-ttu-id="76c88-109">예제 1: 노드 구성 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="76c88-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="76c88-110">이 명령은 NodeConfiguration01 이라는 노드 구성을 지정 된 GUID가 있는 노드에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="76c88-111">변수</span><span class="sxs-lookup"><span data-stu-id="76c88-111">PARAMETERS</span></span>

### <span data-ttu-id="76c88-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76c88-112">-AutomationAccountName</span></span>
<span data-ttu-id="76c88-113">이 cmdlet이 구성을 수정 하는 DSC 노드를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="76c88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c88-114">-DefaultProfile</span></span>
<span data-ttu-id="76c88-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="76c88-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76c88-116">-Force</span><span class="sxs-lookup"><span data-stu-id="76c88-116">-Force</span></span>
<span data-ttu-id="76c88-117">사용자 확인을 요청 하지 않고 실행할 명령을 ps_force 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-117">ps_force the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c88-118">-Id</span><span class="sxs-lookup"><span data-stu-id="76c88-118">-Id</span></span>
<span data-ttu-id="76c88-119">이 cmdlet이 구성을 수정 하는 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c88-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="76c88-120">-NodeConfigurationName</span></span>
<span data-ttu-id="76c88-121">이 cmdlet이 노드를 매핑하는 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c88-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c88-122">-ResourceGroupName</span></span>
<span data-ttu-id="76c88-123">이 cmdlet이 DSC 노드 구성을 수정 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="76c88-124">-확인</span><span class="sxs-lookup"><span data-stu-id="76c88-124">-Confirm</span></span>
<span data-ttu-id="76c88-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c88-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c88-126">-WhatIf</span></span>
<span data-ttu-id="76c88-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c88-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c88-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c88-129">CommonParameters</span></span>
<span data-ttu-id="76c88-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c88-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c88-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c88-132">입력</span><span class="sxs-lookup"><span data-stu-id="76c88-132">INPUTS</span></span>

### <span data-ttu-id="76c88-133">않아야</span><span class="sxs-lookup"><span data-stu-id="76c88-133">None</span></span>
<span data-ttu-id="76c88-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76c88-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76c88-135">출력</span><span class="sxs-lookup"><span data-stu-id="76c88-135">OUTPUTS</span></span>

### <span data-ttu-id="76c88-136">Microsoft Azure.-DscNode</span><span class="sxs-lookup"><span data-stu-id="76c88-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="76c88-137">상속자</span><span class="sxs-lookup"><span data-stu-id="76c88-137">NOTES</span></span>

## <span data-ttu-id="76c88-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76c88-138">RELATED LINKS</span></span>

[<span data-ttu-id="76c88-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="76c88-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="76c88-140">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="76c88-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="76c88-141">등록 취소-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="76c88-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


