---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205512"
---
# <span data-ttu-id="7bef1-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="7bef1-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="7bef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bef1-102">SYNOPSIS</span></span>
<span data-ttu-id="7bef1-103">Automation 연결 형식을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="7bef1-104">구문</span><span class="sxs-lookup"><span data-stu-id="7bef1-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bef1-105">설명</span><span class="sxs-lookup"><span data-stu-id="7bef1-105">DESCRIPTION</span></span>
<span data-ttu-id="7bef1-106">**Remove-AzAutomationConnectionType** cmdlet은 Azure Automation에서 연결 형식을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="7bef1-107">삭제하는 연결 유형과 연결된 모든 연결은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="7bef1-108">다음 조건을 충족하는 새 연결 형식을 만들지 않는 한 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="7bef1-109">형식의 이름은 원래 연결 유형과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="7bef1-110">형식에는 원래 연결 형식과 동일한 필드 정의가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="7bef1-111">추가 필드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-111">It can have additional fields.</span></span>

## <span data-ttu-id="7bef1-112">예제</span><span class="sxs-lookup"><span data-stu-id="7bef1-112">EXAMPLES</span></span>

### <span data-ttu-id="7bef1-113">예제 1: 연결 유형 제거</span><span class="sxs-lookup"><span data-stu-id="7bef1-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7bef1-114">이 명령은 Contoso17이라는 Automation 계정에서 ContosoConnectionType이라는 연결 형식을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7bef1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bef1-115">PARAMETERS</span></span>

### <span data-ttu-id="7bef1-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7bef1-116">-AutomationAccountName</span></span>
<span data-ttu-id="7bef1-117">이 cmdlet이 연결 형식을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="7bef1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bef1-118">-DefaultProfile</span></span>
<span data-ttu-id="7bef1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7bef1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bef1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7bef1-120">-Force</span></span>
<span data-ttu-id="7bef1-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="7bef1-121">ps_force</span></span>

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

### <span data-ttu-id="7bef1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7bef1-122">-Name</span></span>
<span data-ttu-id="7bef1-123">이 cmdlet에서 제거하는 Automation 연결 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7bef1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bef1-124">-ResourceGroupName</span></span>
<span data-ttu-id="7bef1-125">이 cmdlet이 Automation 연결 유형을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="7bef1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bef1-126">-Confirm</span></span>
<span data-ttu-id="7bef1-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bef1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bef1-128">-WhatIf</span></span>
<span data-ttu-id="7bef1-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7bef1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bef1-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bef1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bef1-131">CommonParameters</span></span>
<span data-ttu-id="7bef1-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bef1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bef1-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7bef1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bef1-134">입력</span><span class="sxs-lookup"><span data-stu-id="7bef1-134">INPUTS</span></span>

### <span data-ttu-id="7bef1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7bef1-135">System.String</span></span>

## <span data-ttu-id="7bef1-136">출력</span><span class="sxs-lookup"><span data-stu-id="7bef1-136">OUTPUTS</span></span>

### <span data-ttu-id="7bef1-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="7bef1-137">System.Void</span></span>

## <span data-ttu-id="7bef1-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7bef1-138">NOTES</span></span>

## <span data-ttu-id="7bef1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bef1-139">RELATED LINKS</span></span>

[<span data-ttu-id="7bef1-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7bef1-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


