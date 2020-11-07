---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710990"
---
# <span data-ttu-id="106af-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="106af-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="106af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="106af-102">SYNOPSIS</span></span>
<span data-ttu-id="106af-103">자동화 계정으로 관리에서 DSC 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="106af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="106af-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="106af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="106af-105">DESCRIPTION</span></span>
<span data-ttu-id="106af-106">**AzureRmAutomationDscNode** Cmdlet은 Azure Automation 계정에의 한 관리에서 Ap (원하는 상태 구성) 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="106af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="106af-107">EXAMPLES</span></span>

### <span data-ttu-id="106af-108">예제 1: Automation 계정 관리에서 Azure DSC 노드 제거</span><span class="sxs-lookup"><span data-stu-id="106af-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="106af-109">이 명령은 Contoso17 이라는 자동화 계정으로 지정 된 GUID가 있는 DSC 노드를 관리에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="106af-110">변수</span><span class="sxs-lookup"><span data-stu-id="106af-110">PARAMETERS</span></span>

### <span data-ttu-id="106af-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="106af-111">-AutomationAccountName</span></span>
<span data-ttu-id="106af-112">이 cmdlet이 DSC 노드를 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="106af-113">-Force</span><span class="sxs-lookup"><span data-stu-id="106af-113">-Force</span></span>
<span data-ttu-id="106af-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="106af-114">ps_force</span></span>

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

### <span data-ttu-id="106af-115">-Id</span><span class="sxs-lookup"><span data-stu-id="106af-115">-Id</span></span>
<span data-ttu-id="106af-116">이 cmdlet이 제거 하는 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106af-117">-ResourceGroupName</span></span>
<span data-ttu-id="106af-118">이 cmdlet이 DSC 노드의 등록을 취소 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="106af-119">-확인</span><span class="sxs-lookup"><span data-stu-id="106af-119">-Confirm</span></span>
<span data-ttu-id="106af-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="106af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="106af-121">-WhatIf</span></span>
<span data-ttu-id="106af-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="106af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="106af-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="106af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106af-124">-DefaultProfile</span></span>
<span data-ttu-id="106af-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="106af-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="106af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106af-126">CommonParameters</span></span>
<span data-ttu-id="106af-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="106af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106af-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106af-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106af-129">입력</span><span class="sxs-lookup"><span data-stu-id="106af-129">INPUTS</span></span>

## <span data-ttu-id="106af-130">출력</span><span class="sxs-lookup"><span data-stu-id="106af-130">OUTPUTS</span></span>

### <span data-ttu-id="106af-131">Microsoft Azure.-DscNode</span><span class="sxs-lookup"><span data-stu-id="106af-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="106af-132">상속자</span><span class="sxs-lookup"><span data-stu-id="106af-132">NOTES</span></span>

## <span data-ttu-id="106af-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="106af-133">RELATED LINKS</span></span>

[<span data-ttu-id="106af-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="106af-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="106af-135">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="106af-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="106af-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="106af-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


