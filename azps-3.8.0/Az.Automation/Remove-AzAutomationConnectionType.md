---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044937"
---
# <span data-ttu-id="67574-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="67574-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="67574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67574-102">SYNOPSIS</span></span>
<span data-ttu-id="67574-103">자동화 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="67574-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67574-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67574-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67574-105">DESCRIPTION</span></span>
<span data-ttu-id="67574-106">**AzAutomationConnectionType** Cmdlet은 Azure Automation에서 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="67574-107">삭제 하는 연결 형식과 연결 된 모든 연결을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67574-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="67574-108">다음 조건을 충족 하는 새 연결 형식을 만들지 않는 한 해당 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="67574-109">형식의 이름은 원본 연결 형식과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="67574-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="67574-110">형식에는 원래 연결 형식과 동일한 필드 정의가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67574-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="67574-111">추가 필드가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67574-111">It can have additional fields.</span></span>

## <span data-ttu-id="67574-112">예제의</span><span class="sxs-lookup"><span data-stu-id="67574-112">EXAMPLES</span></span>

### <span data-ttu-id="67574-113">예제 1: 연결 형식 제거</span><span class="sxs-lookup"><span data-stu-id="67574-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="67574-114">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConnectionType 이라는 연결 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="67574-115">변수</span><span class="sxs-lookup"><span data-stu-id="67574-115">PARAMETERS</span></span>

### <span data-ttu-id="67574-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67574-116">-AutomationAccountName</span></span>
<span data-ttu-id="67574-117">이 cmdlet이 연결 형식을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="67574-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67574-118">-DefaultProfile</span></span>
<span data-ttu-id="67574-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67574-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67574-120">-Force</span><span class="sxs-lookup"><span data-stu-id="67574-120">-Force</span></span>
<span data-ttu-id="67574-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="67574-121">ps_force</span></span>

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

### <span data-ttu-id="67574-122">-이름</span><span class="sxs-lookup"><span data-stu-id="67574-122">-Name</span></span>
<span data-ttu-id="67574-123">이 cmdlet이 제거 하는 자동화 연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="67574-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67574-124">-ResourceGroupName</span></span>
<span data-ttu-id="67574-125">이 cmdlet이 자동화 연결 형식을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="67574-126">-확인</span><span class="sxs-lookup"><span data-stu-id="67574-126">-Confirm</span></span>
<span data-ttu-id="67574-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67574-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67574-128">-WhatIf</span></span>
<span data-ttu-id="67574-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67574-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67574-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67574-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67574-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67574-131">CommonParameters</span></span>
<span data-ttu-id="67574-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67574-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67574-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67574-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67574-134">입력</span><span class="sxs-lookup"><span data-stu-id="67574-134">INPUTS</span></span>

### <span data-ttu-id="67574-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67574-135">System.String</span></span>

## <span data-ttu-id="67574-136">출력</span><span class="sxs-lookup"><span data-stu-id="67574-136">OUTPUTS</span></span>

### <span data-ttu-id="67574-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="67574-137">System.Void</span></span>

## <span data-ttu-id="67574-138">상속자</span><span class="sxs-lookup"><span data-stu-id="67574-138">NOTES</span></span>

## <span data-ttu-id="67574-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67574-139">RELATED LINKS</span></span>

[<span data-ttu-id="67574-140">제거-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="67574-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)

