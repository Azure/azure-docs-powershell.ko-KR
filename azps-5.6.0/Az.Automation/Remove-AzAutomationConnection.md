---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 0534f05bcc59a109851188c8b585badfc90d61c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009968"
---
# <span data-ttu-id="e85ce-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e85ce-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="e85ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e85ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e85ce-103">Automation 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="e85ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="e85ce-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e85ce-105">설명</span><span class="sxs-lookup"><span data-stu-id="e85ce-105">DESCRIPTION</span></span>
<span data-ttu-id="e85ce-106">**Remove-AzAutomationConnection** cmdlet은 Azure Automation에서 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="e85ce-107">예제</span><span class="sxs-lookup"><span data-stu-id="e85ce-107">EXAMPLES</span></span>

### <span data-ttu-id="e85ce-108">예제 1: 연결 제거</span><span class="sxs-lookup"><span data-stu-id="e85ce-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e85ce-109">이 명령은 Contoso17이라는 Automation 계정에서 ContosoConnection이라는 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e85ce-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e85ce-110">PARAMETERS</span></span>

### <span data-ttu-id="e85ce-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e85ce-111">-AutomationAccountName</span></span>
<span data-ttu-id="e85ce-112">이 cmdlet에서 연결을 제거하는 자동화 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="e85ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85ce-113">-DefaultProfile</span></span>
<span data-ttu-id="e85ce-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e85ce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e85ce-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e85ce-115">-Force</span></span>
<span data-ttu-id="e85ce-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e85ce-116">ps_force</span></span>

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

### <span data-ttu-id="e85ce-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e85ce-117">-Name</span></span>
<span data-ttu-id="e85ce-118">이 cmdlet이 제거한 연결의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e85ce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85ce-119">-ResourceGroupName</span></span>
<span data-ttu-id="e85ce-120">이 cmdlet에서 연결을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="e85ce-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e85ce-121">-Confirm</span></span>
<span data-ttu-id="e85ce-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85ce-123">-WhatIf</span></span>
<span data-ttu-id="e85ce-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85ce-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85ce-126">CommonParameters</span></span>
<span data-ttu-id="e85ce-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e85ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85ce-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e85ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85ce-129">입력</span><span class="sxs-lookup"><span data-stu-id="e85ce-129">INPUTS</span></span>

### <span data-ttu-id="e85ce-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e85ce-130">System.String</span></span>

## <span data-ttu-id="e85ce-131">출력</span><span class="sxs-lookup"><span data-stu-id="e85ce-131">OUTPUTS</span></span>

### <span data-ttu-id="e85ce-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="e85ce-132">System.Void</span></span>

## <span data-ttu-id="e85ce-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e85ce-133">NOTES</span></span>

## <span data-ttu-id="e85ce-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e85ce-134">RELATED LINKS</span></span>

[<span data-ttu-id="e85ce-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e85ce-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="e85ce-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e85ce-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


